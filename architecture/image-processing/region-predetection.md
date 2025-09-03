---
layout: default-layout
title: Region-Pre-detection Section - Dynamsoft Capture Vision Architecture
description: This article introduces Region-Pre-detection Section in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /architecture/image-processing/region-predetection.html
---

> *Go to [DCV Architecture](../index.md)*

The following diagram shows how sections connect to each other to form tasks:

```mermaid
flowchart LR;
     A[1.Region Pre-Detection]-->C[2.1.Shared Detection]
     C---D[2.2.Barcode Localization]
     C---E[2.2.Text-line Localization]
     C---F[2.2.Document Detection]
     D---G[3.Barcode Decoding]
     E---H[3.Text-line Recognition]
     F---I[3.Document Normalization]
     style A fill:#f96,stroke:#333,stroke-width:4px
```

In this article, we'll discuss the first section of a task - **Region Pre-Detection**:

# Section 1 - Region Pre-Detection

The purpose of this section is to reduce the overall time cost of the task by finding regions of interest (ROIs) and thus ignoring other parts of the image during subsequent processing. It is not required for the task and can be skipped in many cases.

## Constituting Stages

This section consists of multiple stages:

1. Cropping: to crop out the original ROI *specified* by the user. If not specified, return the original image as a whole.
2. Down-scaling: to down-scale a massive image.
3. Grayscaling: to convert a colour image to grayscale.
4. Transforming: to transform a grayscale image.
5. Pre-Detecting: to pre-detect the regions exhibit specific features.

## Output and Parameters

Each of the five stages has its own output (known as an intermediate result) and a specific parameter that can regulate the operation:

| Stage         | Intermediate Result Type           | Related Parameter                                                                                               |
| ------------- | ---------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Cropping      | `IRUT_COLOUR_IMAGE`                | [`Location`](../../parameters/reference/target-roi-def/location.md)                                             |
| Down-scaling  | `IRUT_SCALED_DOWN_COLOUR_IMAGE`    | [`ScaleDownThreshold`](../../parameters/reference/image-parameter/scale-down-threshold.md)                      |
| Grayscaling   | `IRUT_GRAYSCALE_IMAGE`             | [`ColourConversionModes`](../../parameters/reference/image-parameter/colour-conversion-modes.md)                |
| Transforming  | `IRUT_TRANSFORMED_GRAYSCALE_IMAGE` | [`GrayscaleTransformationModes`](../../parameters/reference/image-parameter/grayscale-transformation-modes.md) |
| Pre-Detecting | `IRUT_PREDETECTED_REGIONS`         | [`RegionPredetectionModes`](../../parameters/reference/image-parameter/region-predetection-modes.md)            |
