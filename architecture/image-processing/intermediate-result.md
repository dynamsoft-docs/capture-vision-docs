---
layout: default-layout
title: Intermediate Result - Dynamsoft Capture Vision Architecture
description: This article introduces Intermediate Result in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /architecture/image-processing/intermediate-result.html
---

# Intermediate Result

`IntermediateResult` record a series of data that produced by the image-processing algorithm. It can be either a image (processed image or even the original image) or significant information extracted from the source image.

* Share the image-processing results that required by different tasks that have the same input and parameter settings.
* Receive data from different sections for further analysis.
* Get, modify and updated the intermediate result to receive better result.

## Produce

Intermediate results are produced by different **stages** of the algorithm. The output of a intermediate result stands for the completion of the corresponding algorithm **stage**.

**Intermediate result produced by different sections:**

* Section 1 - Predetection
  * ColourImageunit
  * ScaledDownColourImageUnit
  * TransformedGrayscaleImageUnit
  * PredetectedRegionsUnit
* Section 2 - Detection
  * Section 2.1 Shared detecting
    * ColourImageUnit
    * GrayscaleImageUnit
    * TransformedGrayscaleImageUnit
    * EnhancedGrayscaleImageUnit
    * BinaryImageUnit
    * TextureDetection resultUnit
    * TextureRemovedGrayscaleImageUnit
    * TextureRemovedBinaryImageUnit
    * TextZonesUnit
    * TextRemovedBinaryImageUnit
  * Section 2.2 (Option 1) Barcode localizing
    * ContoursUnit
    * LineSegmentsUnit
    * CandidateBarcodeZonesUnit
    * LocalizedBarcodesUnit
  * Section 2.2 (Option 2) Document boundary detecting
    * ContoursUnit
    * LineSegmentsUnit
    * LongLinesUnit
    * CornersUnit
    * CandidateQuadEdgesUnit
    * DetectedQuadsUnit
  * Section 2.2 (Option 3) Text line localizing
    * LocalizedTextLinesUnit
* Section 3 Barcode decoding
  * ColourImageUnit
  * GrayscaleImageUnit
  * TransformedGrayscaleImageUnit
  * DeformationResistedBarcodeImageUnit
  * ComplementedBarcodeImageUnit
  * ScaledUpBarcodeImageUnit
  * DecodedBarcodesUnit
* Section 3 Document normalizing
  * NormalizedImagesUnit
* Section 3 Text line recognizing
  * ColourImageUnit
  * GrayscaleImageUnit
  * TransformedGrayscaleImageUnit
  * RecognizedTextLinesUnit

For more details about the image-processing algorithm sections and stages, please refer to the [complete process of algorithm](image-process/index.md).

## Inherit

An algorithm task can inherit the intermediate result of another task when:

* They have the same TargetROIDef.
* The initial part of their image-processing parameters is the same.

## Receive

Intermediate Result Receiver (IRR) is designed for receiving the intermediate results. For each type of the intermediate result, a callback is handled when it is produced. You can receive the result data from the callback methods of the IRR. Currently IRR is the only access for them intermediate results.

## Update

All the available ntermediate results are designed to be mutable. You can update your personally processed result and update via the `IntermediateResultManager`.

## Captured Result VS Intermediate Result

* An `IntermediateResult` is produced by a finalized `algorithm stage`.
* A `CapturedResult` is produced by a finalized `algorithm task`.

* An `algorithm stage` definitely produce an `IntermediateResult`.
* An `algorithm task` might not produce a `CapturedResult`. It whether it is defined in a `TargetROI` that listed in `OutputTargetROINameArray` and whether it is able to produce a `CapturedResult`.

* `IntermediateResult` is produced anyway during the process of algorithm.
* `CapturedResult` must be defined in the template so that it is generated and output.
