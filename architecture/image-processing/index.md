---
layout: default-layout
title: Image-Processing Tasks - Dynamsoft Capture Vision
description: This article introduces all image-processing tasks in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /architecture/image-processing/index.html
---

> *Go back to [DCV Architecture](../index.md)*

# Image-Processing Tasks

There are multiple types of tasks when processing images in the Dynamsoft Capture Vision (DCV) architecture.

## Task Types

The following are the image-processing tasks supported:

| Task Type            | Performed By | Category         | Result Type          |
| :------------------- | :----------- | :--------------- | :------------------- |
| Read Barcodes        | DBR          | Image-Processing | Decoded Barcodes     |
| Recognize Text Lines | DLR          | Image-Processing | Recognized TextLines |
| Normalize a Document | DDN          | Image-Processing | Normalized Image     |

## Divide Task into Sections

An image-processing task can be further divided into three sections.

| Task Type            | Sections                                                         |
| :------------------- | :--------------------------------------------------------------- |
| Read Barcodes        | Region Pre-detection, Barcode Localization, Barcode Decoding      |
| Recognize Text Lines | Region Pre-detection, Text-line Localization, Text-line Recognition |
| Normalize a Document | Region Pre-detection, Document Detection, Document Normalization  |

In total, there are 7 unique image-processing sections, which belong to one of three steps of a task:

- Step one: initial image-processing, trying to find parts of the image, called "regions" that exhibit distinct features that match the result we are trying to obtain. Then these regions are cropped to produce regional images as the final output of this step for the next step to process. There is only one section for this step:
  - [Region Pre-detection](region-predetection.md)
  > 1. If no specific region is found, the entire image is the output.
  > 2. There can be multiple regions found which result in multiple regional images as the output.
- Step two: detecting the precise location, called "zones" of the final results (a barcode, a text-line or a document) on the regional images from step one. Then these zones are cropped to produce zonal images as the final output of step two. This step is one of the following three sections:
  - [Barcode Localization](barcode-localization.md)
  - [Text-line Localization](textline-localization.md)
  - [Document Detection](document-detection.md) (a document refers to an object with a quadrilateral boundary)
  > 1. As seen on the table above, one task will have only one of these sections.
  > 2. As mentioned in [divide section into stages](#divide-section-into-stages), each section is further divided into stages. These three sections in step two starts with the same few stages. Read more on [Shared Detection](shared-detection.md).
- Step three: producing the final results based on the zonal images. This step is one of the following three sections:
  - [Barcode Decoding](barcode-decoding.md)
  - [Text-line Recognition](textline-recognition.md)
  - [Document Normalization](document-normalization.md)
  > As seen on the table above, one task will have only one of these sections.

### Incomplete Task

Usually, a task is complete which means it consists of three consecutive sections. However, it is not always the case. 

1. An incomplete task can be a halfway task which means it starts from step two or even step three and consists of only two or even just one section. Read more about [StartSection](../../parameters/reference/start-section.md).
2. An incomplete task can be a premature task which means it ends early and doesn't produce the final results. Unlike a halfway task which must start at the beginning of a section, a premature task can end at any stage of a section. Read more about [TerminateSetting](../../parameters/reference/terminate-settings.md).

## Divide Section into Stages

Each of the 7 sections mentioned in ["Divide Task into Sections"](#divide-task-into-sections) can be further divided into many stages as shown below:

> Stages shared by Barcode Localization, Text-line Localization and Document Detection are put together for the pseudo type "Shared Partial Section". Read more on [Shared Detection](shared-detection.md)

| Section Type             | Stages                                                                                                                                                                                                                                                                                                                                   |
| :----------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Region Predetection      | IRUT_COLOUR_IMAGE, IRUT_SCALED_DOWN_COLOUR_IMAGE, IRUT_GRAYSCALE_IMAGE, <br /> IRUT_TRANSOFRMED_GRAYSCALE_IMAGE, IRUT_PREDETECTED_REGIONS                                                                                                                                                                                                |
| *Shared Partial Section* | IRUT_COLOUR_IMAGE, IRUT_SCALED_DOWN_COLOUR_IMAGE, IRUT_GRAYSCALE_IMAGE, <br /> IRUT_TRANSOFRMED_GRAYSCALE_IMAGE, IRUT_ENHANCED_GRAYSCALE_IMAGE, IRUT_BINARY_IMAGE, <br /> IRUT_TEXTURE_DETECTION_RESULT, IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE, IRUT_TEXTURE_REMOVED_BINARY_IMAGE, <br /> IRUT_TEXT_ZONES, IRUT_TEXT_REMOVED_BINARY_IMAGE |
| Barcode Localization     | IRUT_CONTOURS, IRUT_LINE_SEGMENTS, IRUT_CANDIDATE_BARCODE_ZONES, <br /> IRUT_LOCALIZED_BARCODES                                                                                                                                                                                                                                          |
| Textline Localization    | IRUT_LOCALIZED_TEXT_LINES                                                                                                                                                                                                                                                                                                                |
| Document Detection       | IRUT_CONTOURS, IRUT_LINE_SEGMENTS, IRUT_LONG_LINES, <br /> IRUT_CORNERS, IRUT_CANDIDATE_QUAD_EDGES, IRUT_DETECTED_QUADS                                                                                                                                                                                                                  |
| Barcode Decoding         | IRUT_COLOUR_IMAGE, IRUT_GRAYSCALE_IMAGE, IRUT_TRANSOFRMED_GRAYSCALE_IMAGE, <br /> IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE, IRUT_COMPLEMENTED_BARCODE_IMAGE, IRUT_SCALED_UP_BARCODE_IMAGE, <br /> IRUT_DECODED_BARCODES                                                                                                                   |
| Textline Recognition     | IRUT_COLOUR_IMAGE, IRUT_GRAYSCALE_IMAGE, IRUT_TRANSOFRMED_GRAYSCALE_IMAGE, <br /> IRUT_RECOGNIZED_TEXT_LINES                                                                                                                                                                                                                             |
| Document Normalization   | IRUT_NORMALIZED_IMAGE                                                                                                                                                                                                                                                                                                                    |

In total, there are 27 unique stages:

- IRUT_COLOUR_IMAGE
- IRUT_SCALED_DOWN_COLOUR_IMAGE
- IRUT_GRAYSCALE_IMAGE
- IRUT_TRANSOFRMED_GRAYSCALE_IMAGE
- IRUT_ENHANCED_GRAYSCALE_IMAGE
- IRUT_PREDETECTED_REGIONS
- IRUT_BINARY_IMAGE
- IRUT_TEXTURE_DETECTION_RESULT
- IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE
- IRUT_TEXTURE_REMOVED_BINARY_IMAGE
- IRUT_CONTOURS
- IRUT_LINE_SEGMENTS
- IRUT_TEXT_ZONES
- IRUT_TEXT_REMOVED_BINARY_IMAGE
- IRUT_CANDIDATE_BARCODE_ZONES
- IRUT_LOCALIZED_BARCODES
- IRUT_SCALED_UP_BARCODE_IMAGE
- IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE
- IRUT_COMPLEMENTED_BARCODE_IMAGE
- IRUT_DECODED_BARCODES
- IRUT_LONG_LINES
- IRUT_CORNERS
- IRUT_CANDIDATE_QUAD_EDGES
- IRUT_DETECTED_QUADS
- IRUT_LOCALIZED_TEXT_LINES
- IRUT_RECOGNIZED_TEXT_LINES
- IRUT_NORMALIZED_IMAGE

These stages are the minimal processing units that can be manipulated. The results from these stages are called [intermediate results](intermediate-result.md). For successive stages, the result of one stage is usually the source object to be processed by the next stage. A user can register listeners to obtain the results for one or multiple stages. DCV also allows the user to manipulate the algorithmic process by changing the result in between stages. Read more on [Intermediate Result Receiver](output.md#intermediate-result-receiver).
