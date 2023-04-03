---
layout: default-layout
title: Dynamsoft Capture Vision Architecture
description: This is the main page of Dynamsoft Capture Vision Architecture. 
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /architecture/index.html
---

# Architecture of Dynamsoft Capture Vision

As a powerful SDK framework used for implementing the functionality to derive meaningful information from images, Dynamsoft Capture Vision (DCV) is designed to adapt to a variety of different image processing scenarios. The architecture easily accommodates both entry-level needs and sophisticated business logic, enabling customers to effortlessly build conceptual prototypes within hours, while leaving the door open for complex customizations for more demanding tasks based on the same code. In this article, we'll take a deep dive into the DCV architecture that makes this possible.

## Architecture Diagram

In the [introduction](../introduction/index.md), we have introduced the following [functional products](../introduction/index.md#functional-products):

- Dynamsoft Barcode Reader (DBR)
- Dynamsoft Label Recognizer (DLR)
- Dynamsoft Document Normalizer (DDN)
- Dynamsoft Code Parser (DCP)
- Dynamsoft Camera Enhancer (DCE)

The diagram below shows the architecture of Dynamsoft Capture Vision (DCV) and how these functional products fit into it:

> There are a few other functional products in the diagram but we can ignore them for now.

![DCV Architecture](assets/dcv-architecture.png)

***Diagram 1: DCV Architecture***

As shown in diagram 1, all functional products are passive in the architecture. In other words, they are either told to perform a task or given the result of another task, both of which are done by the active part of the architecture known as Capture Vision Router (CVR).

## Capture Vision Router

Capture Vision Router (CVR) is the most important part of the DCV architecture. As its names suggests, CVR works as a router or a coordinator. Its major tasks include:

### Get Images from the Image Source  

In the DCV architecture, an image source refers to an object that has implemented the [Image Source Adapter (ISA) interface](std-input.md#image-source-adapter). For example,Dynamsoft Camera Enhancer (DCE) is often used as the image source.

At runtime, CVR accepts an image source and tries to get images from it for the functional products to process. Usually, this is a continuous process which ends when the image source is exhausted.

### Coordinate Image-Processing Tasks

CVR accepts and maintains a list of image-processing settings known as ["CaptureVisionTemplates"](../parameters/file/capture-vision-template.md). Each template defines the tasks to be performed against an image. These tasks may be configured to run in parallel or one after another.

At runtime, CVR selects a CaptureVisionTemplate and analyzes it to build a task workflow, which it then runs for all images acquired from the image source.

- For tasks that can run in parallel, CVR will start to process the next image as long as it has an extra working thread to create a functional product instance. Read more on [Parallel Image Processing](#parallel-image-processing).
- For tasks that must run in a sequence, CVR makes sure of the running order.

> There are two type of tasks. Read more about [Image-Processing Tasks](image-processing/index.md) and [Semantic-Processing Tasks](semantic-processing.md).

### Dispatch Results to Listening Objects

In the DCV architecture, a listening object refers to an object that has implemented either the [Captured Result Receiver (CRR) interface](std-output.md#captured-result-receiver) or [Intermediate Result Receiver (IRR) interface](std-output.md#intermediate-result-receiver).

Results are produced throughout the processing workflow of images. We categorize these results in two types:

1. Final results: also known as "Captured Results". These are the results of completed tasks.
   > There are only 6 types of final results. Read more on [final results](std-output.md#final-results).
2. Intermediate results: these are results produced on multiple check-points of a task.
   > These check points are called "Stages", and there are 27 stages at present. Read more on [divisible task](../parameters/file/task-settings/index.md#divisible-task).

There is no limit to the number of listening objects.

The following diagram is a simple demostration of the process:

![CVR Tasks](assets/CVR-Tasks.png)

***Diagram 2: CVR Tasks***

## Architecture Advantages

With the help of CVR, the DCV architecture has the following advantages:

> These advantages were previously introduced as [DCV Key Features](../introduction/index.md#key-features).

### Scalability with Pluggable Components

In the architecture, scalability is demonstrated in the following aspects:

1. The "source" that supplies images to be processed can be any object that is compliant with the [Image Source Adapter (ISA) interface](std-input.md#image-source-adapter).
  > ISA is an open interface, and Dynamsoft provides a skeleton implementation based on which customers can build their own image sources. For example, one that supplies images on the cloud.
  > 
  > Customers can also choose to use the following options:
  > - **Dynamsoft Camera Enhaner**, a product that supplies frames from a live video stream
  > - **Directory Fetcher**, a utility class that supplies existing images from a directory
2. Depending on the business requirments, CVR can use only one or up to all four functional products to perform tasks on the same images and produce multiple kinds of results.
  > CVR takes care of task coordination internally, which means the customer application can use the same API to get different results.
3. The results from processing the same images can be reused multiple times simply by adding more listener objects.

### Flexibility With Customizable Workflows

In the DCV architecure, flexibility is achieved through task coordination.

Task coordination is a process in which CVR establishes a workflow connecting different tasks, and then calls upon corresponding functional products to perform these tasks against each image.

Let's take the following sample image as an example

![sample-image](assets/sample-image-requirements.jpg)

***Figure 1: Sample Image***

The requirements are:

1. Accurately find the boundary of the patient **form** and normalize it. This is a DDN task.
2. Read the barcode **on the form** to get the patient id. This is a DBR task.
3. Read the text **above the barcode** to determine whether the patient has tested positive for Covid-19. This is a DLR task.

Diagram 3 is a simple demonstration of the coordination:

![CVR-Task-Coordination](assets/CVR-Tasks-Coordination.png)

***Diagram 3: CVR Task Coordination***

### High Performance With Shared Computations

With multiple functional products working together in the DCV architecture guided by CVR, it is possible to achieve maximized performance. The reason behind lies in the ideas of "Intermediate Results Sharing" and "Parallel image processing".

#### **Intermediate Results Sharing**

When talking about how CVR ["Dispatch Results to Listening Objects"](#dispatch-results-to-listening-objects), we mentioned intermediate results which are produced on multiple check-points, known as stages, of a task. Then from ["Coordinate Image-Processing Tasks"](#coordinate-image-processing-tasks), we know that multiple tasks can be configured in one image-processing workflow. Take the "Sample Image" processing we just demostrated as an example, the image is first processed by DDN, then by DBR, lastly by DLR. All three tasks analyze the pixels of an image to find results, and they share similar analysis "stages". Under certain conditions, they can share the results of these stages, saving unnecessary computations and time.

The following diagram is a simple demonstration of the idea:

![Intermediate-Result-Sharing](assets/Intermediate-Result-Sharing.png)

***Diagram 4: Intermediate Results Sharing***

In the diagram, the assumptions are that all three tasks share stage 1 while DDN & DBR also share stage 2. When the workflow starts running, the following may happen:

1. The DDN task performs operations for all 3 stages;
2. The DBR task directly uses results from the DDN task for stage 1 & 2 and only needs to perform operation for stage 3;
3. The DLR task directly uses the result from the DDN task and only needs to perform operations for stage 2 & 3.

> NOTE
> 1. Usually there are far more than 3 stages per task.
> 2. In real time, it is also likely for an early task to use the intermediate result of a later task.

#### **Parallel image processing**

As shown above in diagram 3, CVR maintains a pool of instances containing functional product instances that can be invoked immediately for certain tasks. At runtime, CVR will keep trying to get images from the image source and will try to start processing a new image as long as there is at least one idle functional instance to use.

> An instance in the pool can be any instance (DBR/DDN/DLR/DCP) at any given time. This is determined and maintained by CVR at runtime.

### Simplicity with Packable Scenarios

Another benefit of the DCV Architecture is that the outward interface is very simple. Let's revisit the three jobs for CVR introduced above (refer to [Capture Vision Router](#capture-vision-router) and "Diagram 2"):

| Index | Description                            | Corresponding API of CVR                                                                                                               |
| :-------- | :------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| Job 1     | Get Images from the Image Source.      | `SetInput()` accepts an image source.                                                                                                  |
| Job 2     | Coordinate Image-Processing Tasks.     | `InitSettings()` accepts a parameter file which defines one or multiple worflows and `StartCapturing()` specifies one workflow to use. |
| Job 3     | Dispatch Results to Listening Objects. | `AddResultReceiver()` accepts one or multiple listening objects.                                                                       |

Job 1 and 3 serve as "input" and "output" and are very straightforward. In different applications, the real difference is in job 2 where different arrangements of tasks mean the applications may do completely different things. For some usage scenarios, the workflows are usually consistent, which allows settings to be predefined as ["CaptureVisionTemplates"](../parameters/file/capture-vision-template.md) for them. We call these scenarios packable scenarios. Customers can specify one of these templates to use in their applications, thus dramatically simplifies their development.

### Bidirectional Interactivity with Intermediate Results

In the process of deriving meaningful information from images, interaction is usually required. With the help of intermediate results, the DCV architecture facilitates the interfaction in the following ways:

#### **Timely dispatch of intermediate results**

Each image-processing task consists of multiple stages. Each stage is itself a substantial operation. For example, one stage may convert a colour image to grayscale and the next stage binarize the grayscale image. Some of these results may not be very useful. However, let's consider the barcode reading process, one stage may find the exact location of a barcode and another may decode the barcode to get the text. In some cases, a barcode may be localized but fail to be decoded and we want the user to notice the difference. To do this, we add a listening object compatible with the [Intermediate Result Receiver (IRR) interface](std-output.md#intermediate-result-receiver) and listen for localized barcodes and decoded barcodes, then mark these barcodes with different colours.

Intermediate results are generated throughout the execution of a task and CVR makes sure that these results are immediately dispatched to all registered listeners. The following diagram is a simple demostration of this.

![Intermediate-Result-Dispatch](assets/Intermediate-Result-Dispatch.png)

***Diagram 5: Intermediate Results Dispatching***

#### **Elective intervention of the processing workflow**

The DCV architecture allows external programs to intervene in image processing. The steps are

1. A specific type of intermediate result is generated;
2. CVR dispatches the result to a registered listener A and pauses image processing;
3. Customer's code in the callback function for listner A receives the result;
4. The code examines the result, make some changes and send it back to CVR;
5. CVR injects the updated data back and resumes image processing.
  
The following diagram is a simple demostration of this process

![Intermediate-Result-Intervention](assets/Intermediate-Result-Intervention.png)

***Diagram 6: Intermediate Results Intervention***
