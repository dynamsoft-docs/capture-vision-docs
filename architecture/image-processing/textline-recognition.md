---
layout: default-layout
title: Text-line Recognition Section - Dynamsoft Capture Vision Architecture
description: This article introduces Text-line Recognition Section in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /architecture/image-processing/textline-recognition.html
---

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
     style H fill:#f96,stroke:#333,stroke-width:4px
```

In this article, we'll discuss the section **Text-line Recognition** which is usually the 3rd section of a "Recognize-Text-Lines" task.

# Section 3 - Text-line Recognition

The purpose of this section is to recognize the text from the text-line areas identified in the previous section "Text-line Localization".

## Constituting Stages

This section consists of the following stages:

1. Cropping: to cut out the text-line areas based on text-line localization results. This results in one or multiple colour images.
2. Grayscaling: to convert the colour image(s) to grayscale.
3. Transforming: to transform the grayscale image(s).
4. Text-line-recognizing: to recognize the text.

## Output and Parameters

Each of these stages has its own output (known as an intermediate result) and usually a specific parameter that can regulate the operation:

| Stage                 | Intermediate Result Type           | Related Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| --------------------- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Cropping              | `IRUT_COLOUR_IMAGE`                | N/A                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Grayscaling           | `IRUT_GRAYSCALE_IMAGE`             | [`ColourConversionModes`](../../parameters/reference/image-parameter/colour-conversion-modes.md)                                                                                                                                                                                                                                                                                                                                                                    |
| Transforming          | `IRUT_TRANSFORMED_GRAYSCALE_IMAGE` | [`GrayscaleTransformationModes`](../../parameters/reference/image-parameter/grayscale-transformation-modes.md)                                                                                                                                                                                                                                                                                                                                                      |
| Text-line-recognizing | `IRUT_RECOGNIZED_TEXT_LINES`       | [`DictionaryPath`](../../parameters/reference/label-recognizer-task-settings/dictionary-path.md) <br> [`DictionaryCorrectionThresholds`](../../parameters/reference/label-recognizer-task-settings/dictionary-correction-thresholds.md) <br> [`StringLengthRange`](../../parameters/reference/label-recognizer-task-settings/string-length-range.md) <br> [`StringRegExPattern`](../../parameters/reference/label-recognizer-task-settings/string-regex-pattern.md) |
