---
layout: default-layout
title: BarcodeReaderTaskSetting Parameters - Dynamsoft Capture Vision
description: Reference index for BarcodeReaderTaskSetting parameters in Dynamsoft Capture Vision, including barcode format, localization, deformation resisting, deblur, and DPM code reading settings.
keywords: BarcodeReaderTaskSetting, barcode reader, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# BarcodeReaderTaskSetting Parameters

The `BarcodeReaderTaskSetting` object configures settings for barcode reading tasks performed on images in Dynamsoft Capture Vision. Below is the full list of available parameters.

## General

| Parameter | Description |
|:----------|:------------|
| [`Name`](name.html) | The name of the BarcodeReaderTaskSetting object. |
| [`BaseBarcodeReaderTaskSettingName`](base-barcode-reader-task-setting-name.html) | The name of another BarcodeReaderTaskSetting object to inherit from. |
| [`MaxThreadsInOneTask`](max-threads-in-one-task.html) | The maximum threads in one barcode reading task. |

## Barcode Format & Result

| Parameter | Description |
|:----------|:------------|
| [`BarcodeFormatIds`](barcode-format-ids.html) | The target barcode formats to read. |
| [`BarcodeFormatSpecificationNameArray`](barcode-format-specification-name-array.html) | The names of BarcodeFormatSpecification objects to reference. |
| [`ExpectedBarcodesCount`](expected-barcodes-count.html) | The expected number of barcodes to read. |
| [`ReturnBarcodeZoneClarity`](return-barcode-zone-clarity.html) | Whether to return the clarity of the barcode zone. |
| [`TextResultOrderModes`](text-result-order-modes.html) | The order modes for text results. |
| [`BarcodeComplementModes`](barcode-complement-modes.html) | The modes for complementing incomplete barcodes. |
| [`BarcodeScaleModes`](barcode-scale-modes.html) | The modes for scaling barcodes. |

## Processing Modes

| Parameter | Description |
|:----------|:------------|
| [`LocalizationModes`](localization-modes.html) | The modes for barcode localization. |
| [`DeblurModes`](deblur-modes.html) | The modes for deblurring barcode zones. |
| [`DeformationResistingModes`](deformation-resisting-modes.html) | The modes for resisting barcode deformation. |
| [`DPMCodeReadingModes`](dpm-code-reading-modes.html) | The modes for reading DPM (Direct Part Marking) codes. |

## Section & Stage Configuration

| Parameter | Description |
|:----------|:------------|
| [`SectionArray`](section-array.html) | The sections of the barcode reading task. |
| [`SectionRegionPredetection`](section-region-predetection.html) | Region predetection section settings. |
| [`SectionBarcodeLocalization`](section-barcode-localization.html) | Barcode localization section settings. |
| [`SectionBarcodeDecoding`](section-barcode-decoding.html) | Barcode decoding section settings. |
| [`StagePredetectRegions`](stage-predetect-regions.html) | Stage for predetecting regions. |
| [`StageLocalizeCandidateBarcodes`](stage-localize-candidate-barcodes.html) | Stage for localizing candidate barcodes. |
| [`StageLocalizeBarcodes`](stage-localize-barcodes.html) | Stage for localizing barcodes. |
| [`StageScaleBarcodeImage`](stage-scale-barcode-image.html) | Stage for scaling barcode images. |
| [`StageResistDeformation`](stage-resist-deformation.html) | Stage for resisting deformation. |
| [`StageComplementBarcode`](stage-complement-barcode.html) | Stage for complementing barcodes. |
| [`StageDecodeBarcodes`](stage-decode-barcodes.html) | Stage for decoding barcodes. |
