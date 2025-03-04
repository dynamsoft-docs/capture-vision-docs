---
layout: default-layout
title: Image-Processing Tasks - Dynamsoft Capture Vision Architecture
description: This article introduces all image-processing tasks in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
---

# Image-Processing Tasks

In the Dynamsoft Capture Vision (DCV) architecture, various image-processing tasks exist, each representing a comprehensive algorithmic procedure designed to extract specific information or enhance the original image.

## Tasks

The following image-processing tasks are currently supported:

- Read barcodes
- Recognize text lines
- Normalize a document

## Sections and stages

Each image-processing task consists of multiple sections, with each section containing algorithmic procedures that generate location-based results. Additionally, each section is further divided into multiple stages.

The sections for each task are listed below. To learn more about the stages within each section, follow the provided links.

### Read barcodes

This task includes the following sections:

- [Region pre-detection](../../parameters/reference/barcode-reader-task-settings/section-region-predetection.md)
- [Barcode localization](../../parameters/reference/barcode-reader-task-settings/section-barcode-localization.md)
- [Barcode decoding](../../parameters/reference/barcode-reader-task-settings/section-barcode-decoding.md)

### Recognize text lines

This task includes the following sections:

- [Region pre-detection](../../parameters/reference/label-recognizer-task-settings/section-regions-predetection.md)
- [Text-line localization](../../parameters/reference/label-recognizer-task-settings/section-text-lines-localization.md)
- [Text-line recognition](../../parameters/reference/label-recognizer-task-settings/section-text-lines-recognition.md)

### Normalize a document

This task includes the following sections:

- [Region pre-detection](../../parameters/reference/document-normalizer-task-settings/section-regions-predetection.md)
- [Document detection](../../parameters/reference/document-normalizer-task-settings/section-document-detection.md)
- [Document deskewing](../../parameters/reference/document-normalizer-task-settings/section-document-deskewing.md)
- [Image enhancement](../../parameters/reference/document-normalizer-task-settings/section-image-enhancement.md)

## Stages and intermediate results

Stages are the smallest processing units in the workflow, and their outputs are referred to as intermediate results. The result of one stage typically serves as the input for the next.

Users can register listeners to capture results from one or multiple stages. DCV also allows real-time intervention, enabling users to modify the algorithmic process by adjusting intermediate results between stages.

For more details, refer to:

- [Intermediate result receiver](../output.md#intermediate-result-receiver)  
- [Bidirectional interactivity with intermediate results](../index.md#bidirectional-interactivity-with-intermediate-results)  
