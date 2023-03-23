---
layout: default-layout
title: Intermediate Result
description: This page introduce how intermediate result is designed in Dynamsoft Capture Vision.
keywords: document detetion
needAutoGenerateSidebar: true
breadcrumbText: Intermediate Result
---

# Intermediate Result

Intermediate result is one of the basic concept of Dynamsoft Capture Vision.

* Share the image processing results that required by different tasks that have the same input and parameter settings.
* Receive data from different sections for further analysis.
* Get, modify and updated the intermediate result to receive better result.

## Produce & Inherit

Intermediate results are produced by different stages of the algorithm. The output of a intermediate result stands for the completion of the corresponding algorithm stage.

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

## Receive

Intermediate Result Receiver (IRR) is designed for receiving the intermediate results. For each type of the intermediate result, a callback is handled when it is produced. You can receive the result data from the callback methods of the IRR. Currently IRR is the only access for them intermediate results.

## Update

All the available ntermediate results are designed to be mutable. You can update your personally processed result and update via the `IntermediateResultManager`.

## Captured Result VS Intermediate Result

The output of a **Capture Result** stands for the finalize of a algorithm **task** while the output of an **Intermediate Result** stands for the finalize of an algorithm **stage**.
