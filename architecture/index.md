---
layout: default-layout
title: Dynamsoft Capture Vision Architecture  - Main Page
description: This is the main page of Dynamsoft Capture Vision Architecture. 
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /architecture/index.html
---

# Architecture of Dynamsoft Capture Vision

Dynamsoft Capture Vision (DCV) is designed for simplicity, flexibility, scalability and high performance.

## Simplicity

In short, DCV is used to derive meaningful information from images. Therefore, it essentially consists of three components:

1. Image source  
   An image source acquires and supplies images to DCV to process. In the DCV architecture, an image source is an object that has implemented the Image Source Adapter (ISA) interface.
2. Image processing unit  
   The image processing unit is the most important part in the DCV architecture. It processes each image from the image source according to a  predefined settings and outputs the results to each Information output object.
   Semantic processing is an auxiliary and optional step that helps parse instant text results from the image into human-readable data tables.
3. Information output object  
   An information output object receives the information DCV has derived from the images. In the DCV architecture, such an object is one that has implemented either the Captured Result Receiver (CRR) interface or Intermediate Result Receiver (IRR) interface.

![An image depicting the 3 components]()

### Capture Vision Router

Capture Vision Router (CVR) is the central piece in the DCV architecutre. It has two jobs:

1. Connect the components  
   CVR is the one that 
2. Manage the workflow  
   CVR is the one that drives...

## Flexibility

The flexibility of the DCV architecture is demonstrated through the highly customizable workflows in processing an image. A workflow consists of one or many tasks which are performed by functional modules including Dynamsoft Barcode Reader (DBR), Dynamsoft Document Normalizer (DDN), Dynamsoft Label Recognizer (DLR) and Dynamsoft Code Parser (DCP). These tasks can be set in a number of different ways, for example:

1. Independent tasks that can run in parallel; 
2. Consecutive tasks where latter tasks depend on their previous ones.

There is also no restriction on how many tasks of the same type (performed by the same functional module) can be set in one workflow.

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

### List of modules

1. Dynamsoft License (DL)
2. Dynamsoft Core (DC)
3. Capture Vision Router (CVR)
4. Dynamsoft Camera Enhancer (DCE)
5. Dynamsoft Barcode Reader (DBR)
6. Dynamsoft Document Normalizer (DDN)
7. Dynamsoft Label Recognizer (DLR)
8. Dynamsoft Code Parser (DCP)
9. Dynamsoft Utility (DU)

## High Performance

The DCV architecture ensures high performance by the following means:

1. Parallel execution of independent tasks;
2. Shared computations when different processing steps require the same (part of an) image to be processed in the same way;
3. Non-stopping supply of images which ensures the image processing unit doesn't need to wait.