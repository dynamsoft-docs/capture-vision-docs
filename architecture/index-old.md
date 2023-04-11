---
layout: default-layout
title: Dynamsoft Capture Vision Architecture
description: This is the main page of Dynamsoft Capture Vision Architecture. 
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /architecture/index-old.html
---

# Architecture of Dynamsoft Capture Vision

Dynamsoft Capture Vision (DCV) is a powerful SDK framework used to implement the functionality to derive meaningful information from images in all kinds of applications. 

The framework is designed to adapt to a variety of different image processing scenarios. The structure easily accommodates both entry-level needs and sophisticated business logic, enabling customers to effortlessly build conceptual prototypes within hours, while leaving the door open for complex customizations for more demanding tasks based on the same code.

This article presents the DCV architecture, which explains why it has the following advantages:

1. Low barriers to entry for image processing
2. Flexible expansion of its functionality
3. Agile capability for fine-grained process control

**Table of Contents**

- [Concise Structure](#concise-structure)
- [Independent Modules](#independent-modules)
  - [Capture Vision Router](#capture-vision-router)
  - [Dynamsoft License](#dynamsoft-license)
  - [Dynamsoft Utility](#dynamsoft-utility)
- [Customizable Workflow](#customizable-workflow)
  - [Task Types](#task-types)
  - [Target Region Of Interest](#target-region-of-interest)
  - [Semantic Processing Options](#semantic-processing-options)

## Concise Structure

At the top level, the DCV architecture consists of three components:

1. Image Source  
   An image source acquires and supplies images to DCV to process. In the DCV architecture, an image source is an object that has implemented the [Image Source Adapter (ISA) interface](input.md#image-source-adapter).
2. Image Processing Unit  
   The image processing unit is the most important part in the DCV architecture. It processes each image from the image source according to a predefined settings and outputs the results to each information output object.
   Semantic processing is an auxiliary and optional step that helps parse instant text results from the image into human-readable data tables.
3. Information Output Target  
   An information output target receives the information DCV has derived from the images. In the DCV architecture, such an object is one that has implemented either the [Captured Result Receiver (CRR) interface](output.md#captured-result-receiver) or [Intermediate Result Receiver (IRR) interface](output.md#intermediate-result-receiver).

![An image depicting the 3 components]()

## Independent Modules

To create a solution under the DCV structure, we need to combine a few functional modules. The following shows the modules that support the DCV structure:


| Module Name                   | Abbreviation | Description                                                                     | Role in the Structure                   |
| :---------------------------- | :----------: | :------------------------------------------------------------------------------ | :-------------------------------------- |
| Dynamsoft License             |    **DL**    | Provides license control.                                                       | Auxiliary                               |
| Dynamsoft Core                |    **DC**    | Provides basic data structures and intermediate result structures.              | Image Processing Unit                   |
| Capture Vision Router         |   **CVR**    | Connects components and coordinates the complete workflow.                      | Manager, Coordinator                    |
| Dynamsoft Camera Enhancer     |   **DCE**    | Provides camera control and basic user interface.                               | Image Source, Information Output Target |
| Dynamsoft Barcode Reader      |   **DBR**    | Provides barcode reading capabilities.                                          | Image Processing Unit                   |
| Dynamsoft Document Normalizer |   **DDN**    | Provides structure analysis, document detection and normalization capabilities. | Image Processing Unit                   |
| Dynamsoft Label Recognizer    |   **DLR**    | Provides simple text recognition capabilities.                                  | Image Processing Unit                   |
| Dynamsoft Code Parser         |   **DCP**    | Provides the ability to parse codes of certain standards.                       | Image Processing Unit                   |
| Dynamsoft Utility             |    **DU**    | Provides official utilities.                                                    | Image Source, Auxiliary                 |

As shown in the table, these modules don't belong to any of the three components: Dynamsoft License, Capture Vision Router and Dynamsoft Utility. We will talk about them first.

### Capture Vision Router

Of all the modules, Capture Vision Router (CVR) is the central piece in the DCV architecutre. It has the following jobs:

1. Connect the Components  
   The three components "Image Source", "Image Processing Unit" and "Information Output Target" are connected by CVR like this
   - CVR accepts an object as the "Image Source", from which it proactively requests images at runtime for the "Image Processing Unit" to process
   - CVR accepts and maintains a list of image-processing workflow settings known as ["CaptureVisionTemplates"](../parameters/file/CaptureVisionTemplate.md). CVR usually use only one of the settings to set up the "Image Processing Unit" for processing the images from the "Image Source"
   - CVR accepts one or more objects as the "Information Output Target" to receive results produced by the "Image Processing Unit"
2. Manage the Process  
   After connecting the three components, CVR is also the one that drives the entire process forward. Its jobs include
   - Starting the process. This means a few things
     - CVR determines which funtional modules are required by analyzing the selected "CaptureVisionTemplate" and gets them loaded
     - CVR signals the "Image Source" to start acquiring images into its buffer if it hasn't started yet
     - CVR requests images from the "Image Source" one by one and passes them to the "Image Processing Unit"
   - Coordinating tasks. This indicates
     - CVR analyzes the selected "CaptureVisionTemplate" and establishes a list of tasks which must be performed on every image
     - CVR processes each image according to the established list of tasks
     - For a multi-thread application, as soon as a thread becomes idle, CVR assigns it a new image to process
   - Triggering result listeners
     - Each "Information Output Target" will register one or several result listeners with CVR. Whenever an "image processing unit" produces a result of a certain type, the CVR triggers all listeners of that type to pass the result out

### Dynamsoft License

As the name suggests, this module is responsible for licensing the SDK framework, which is a mandatory step before any feature can be used.

### Dynamsoft Utility

This module contains miscellaneous utility classes. For example, it provides a `DirectoryFetcher` class which is able to convert a local file directory as an "Image Source".

## Customizable Workflow

As mentioned above, a ["CaptureVisionTemplate"](../parameters/file/CaptureVisionTemplate.md) defines a complete image-processing workflow that an image goes through when processed by DCV. One or multiple such templates are defined in a [parameter file](../parameters/file/index.md) which is entered into a DCV instance. However, only one template is used when DCV starts an image-processing job.

A workflow may contain multiple tasks of different types that can be configured to run in parallel or one after another.

### Task Types

There are five types of tasks and they belong to two categories: image processing tasks and semantic processing tasks.

> NOTE
> 
> 1. All tasks are optional.
> 2. A semantic-processing task always happens after another image-processing task.

| Task Type            | Performed By | Category            | Result Type          |
| :------------------- | :----------- | :------------------ | :------------------- |
| Read Barcodes        | DBR          | Image Processing    | Decoded Barcodes     |
| Recognize Text Lines | DLR          | Image Processing    | Recognized TextLines |
| Normalize a Document | DDN          | Image Processing    | Normalized Image     |
| Parse Text           | DCP          | Semantic Processing | Parse Result Object  |

### Target Region Of Interest

The most important concept in a CaptureVisionTemplate is "Target Region Of Interest" (TargetROI for short). As its name suggests, TargetROI defines a part of an image as the target for performing one or multiple tasks.

A TargetROI is usually defined like this:

```json
{
   "Name": "TargetROI-Definition-Sample",
   "Location": {},
   "TaskSettingNameArray": ["Task-A", "Task-B"]
},
```

As shown above, a definition consists of three integral aspects:

1. "Name" is a unique string to identify the TargetROI
2. "Location" defines which part of the image is processed
3. "TaskSettingNameArray" specifies what tasks are to be performed by referring to their names. These tasks are limited to the "Image Processing" category. Check [Task Types](#task-types) above for more information.

"Name" and "TaskSettingNameArray" are very easy to understand. "Location", on the other hand, is much more complicated. The following shows how "Location" is defined:

```json
"Location": {
   "ReferenceObjectFilter": {},
   "Offset": {}
}
```

In the definition, "ReferenceObjectFilter" specifies which objects can be used as reference to calculate the actual location while `Offset` specifies how the location is calculated. Read more about ["ReferenceObjectFilter"](../parameters/file/../reference/reference-object-filter.md).

In order to be valid, reference objects usually provide their own coordinates in the form of quadrilaterals. Such objects include the original image, a localized/decoded barcode, a detected boundary of an object or a localized/recoginzed textline. **Note that these objects are very likely the results of tasks on another TargetROI! In other words, one TargetROI may be configured to process a part of the image, which is calculated based on the coordinates of the process result of another TargetROI. This is how we can establish a series of tasks where a latter task depends on a former one to simulate the natural way of thinking when trying to find a specific piece of information.**

> "ReferenceObjectFilter" may contain multiple objects, which in turn can specify multiple parts of the image on which all tasks specified by "TaskSettingNameArray" are performed.

### Semantic Processing Options

Semantic processing usually works on a string and is most likely the last step in a workflow. It is linked to other TargetROI definitions by specifying which TargetROI generates the string(s) for it to process. Semantic processing operations are defined as Semantic Processing Options and each option is defined like this:

```json
{
    "Name": "Semantic-Processing-Option-Sample",
    "ReferenceObjectFilter": {},
    "TaskSettingNameArray": [ "Parse-Task-1" ]
}
```

"ReferenceObjectFilter" is the same as the one mentioned in [Target Region Of Interest](#target-region-of-interest) but the difference is the resulting "reference objects" must be a text which can be parsed.

"TaskSettingNameArray" must specify a text-parsing task.

Read more about [semantic processing](semantic-process.md).

With TargetROI definitions and semantic processing options, a CaptureVisionTemplate is able to establish a customized workflow with organzied tasks to process images and obtain different types of results.
