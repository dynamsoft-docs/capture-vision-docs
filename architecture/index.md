---
layout: default-layout
title: Dynamsoft Capture Vision Architecture
description: This is the main page of Dynamsoft Capture Vision Architecture. 
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /architecture/index.html
---

# Architecture of Dynamsoft Capture Vision

Dynamsoft Capture Vision (DCV) is a powerful SDK framework used to implement the functionality to derive meaningful information from images in all kinds of applications. 

The framework is designed to adapt to a variety of different image processing scenarios. The structure easily accommodates both entry-level needs and sophisticated business logic, enabling customers to effortlessly build conceptual prototypes within hours, while leaving the door open for complex customizations for more demanding tasks based on the same code.

This article presents the DCV architecture, which explains why it has the following advantages:

1. Low barrier of entry to image processing
2. Easy to extend functionality
3. Capable of finely-controlling the process 

## Simple and Concise Structure

At the top level, the DCV architecture consists of three components:

1. Image Source  
   An image source acquires and supplies images to DCV to process. In the DCV architecture, an image source is an object that has implemented the [Image Source Adapter (ISA) interface](std-input.md#image-source-adapter).
2. Image Processing Unit  
   The image processing unit is the most important part in the DCV architecture. It processes each image from the image source according to a predefined settings and outputs the results to each information output object.
   Semantic processing is an auxiliary and optional step that helps parse instant text results from the image into human-readable data tables.
3. Information Output Target  
   An information output target receives the information DCV has derived from the images. In the DCV architecture, such an object is one that has implemented either the [Captured Result Receiver (CRR) interface](std-output.md#captured-result-receiver) or [Intermediate Result Receiver (IRR) interface](std-output.md#intermediate-result-receiver).

![An image depicting the 3 components]()

## Independent Modules

To create a solution under the DCV structure, we need to combine a few functional modules. The following shows the modules that support the DCV structure:


| Module Name                   | Abbreviation | Description                                                                     | Role in the Structure   |
| :---------------------------- | :----------: | :------------------------------------------------------------------------------ | :---------------------- |
| Dynamsoft License             |    **DL**    | Provides license control.                                                       | Auxiliary               |
| Dynamsoft Core                |    **DC**    | Provides basic data structures and intermediate result structures.              | Image Processing Unit   |
| Capture Vision Router         |   **CVR**    | Connects components and coordinates the complete workflow.                      | Manager, Coordinator    |
| Dynamsoft Camera Enhancer     |   **DCE**    | Provides camera control and basic user interface.                               | Image Source, Basic UI  |
| Dynamsoft Barcode Reader      |   **DBR**    | Provides barcode reading capabilities.                                          | Image Processing Unit   |
| Dynamsoft Document Normalizer |   **DDN**    | Provides structure analysis, document detection and normalization capabilities. | Image Processing Unit   |
| Dynamsoft Label Recognizer    |   **DLR**    | Provides simple text recognition capabilities.                                  | Image Processing Unit   |
| Dynamsoft Code Parser         |   **DCP**    | Provides the ability to parse codes of certain standards.                       | Image Processing Unit   |
| Dynamsoft Utility             |    **DU**    | Provides official utilities.                                                    | Image Source, Auxiliary |

### Capture Vision Router

Of the 9 modules, Capture Vision Router (CVR) is the central piece in the DCV architecutre. It has the following jobs:

1. Connect the components  
   CVR is the one that drives the 
2. Manage the workflow  
   CVR is the one that drives...

## Scalability

The DCV architecture is not a static system. Different solutions may require different combinations of the modules which support the architecture (see below [the list of the modules](#list-of-modules)). For example:

| Solution Requirements                                        | Required Modules                      |
| :----------------------------------------------------------- | :------------------------------------ |
| Capture images from a camera.                                | DL + DCE                              |
| Capture high-quality documents from a camera.                | DL + DC + CVR + DCE + DDN             |
| Read Barcodes from existing images.                          | DL + DC + CVR + DU + DBR              |
| Real-time barcode detection from a camera.                   | DL + DC + CVR + DCE + DBR             |
| Real-time MRZ recognition from a camera.                     | DL + DC + CVR + DCE + DLR + DCP       |
| Real-time Driver's license recognition from a camera.        | DL + DC + CVR + DCE + DBR + DCP       |
| Real-time recognition of form fields which include barcodes. | DL + DC + CVR + DCE + DDN + DLR + DBR |

#