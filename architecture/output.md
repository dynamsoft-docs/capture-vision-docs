---
layout: default-layout
title: Standard Output - Dynamsoft Capture Vision Architecture
description: This article is about the standard output in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /architecture/output.html
---

# Output

![DCV Architecture](assets/dcv-architecture-output.png)

As the final component of the **Dynamsoft Capture Vision (DCV) architecture**, the output system is responsible for delivering image-processing results to objects that depend on them.

A standard output target is any object that implements either the [Captured Result Receiver (CRR) interface](#captured-result-receiver) or the [Intermediate Result Receiver (IRR) interface](#intermediate-result-receiver). Both interfaces consist of multiple callback functions, making an output target commonly referred to as a **listening object**.

## Captured Result Receiver

The **Captured Result Receiver (CRR)** interface handles the output of *final results*.

### Final Results

Final results refer to the following types of processed outputs:

1. The original image  
2. Barcode text found on the image  
3. Text lines found on the image  
4. Document boundaries found on the image  
5. An enhanced image
6. A cropped and deskewed image based on a detected document boundary  
7. Data tables parsed from barcode text or recognized text lines  

These results are considered *final* because they are returned **only after** an image has been fully processed. For each image, CRR callback functions are triggered only once.

## Intermediate Result Receiver

The **Intermediate Result Receiver (IRR)** interface handles the output of **intermediate results**. These results are considered **intermediate** because they are generated during the processing of an image, before final results are produced.  

Unlike the final results, intermediate results are returned as soon as they are available.

> **Note for JavaScript Edition:** Due to technical restrictions, intermediate results are currently returned only after the image has finished processing.
