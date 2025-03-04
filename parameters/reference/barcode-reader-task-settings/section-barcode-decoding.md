---
layout: default-layout
title: BarcodeDecodingSection Object - Dynamsoft Barcode Reader Parameters
description: This page defines BarcodeDecodingSection Object under the BarcodeReaderTaskSetting.
keywords: BarcodeDecodingSection Object
---

# BarcodeDecodingSection Object

The `BarcodeDecodingSection` object is designed to define the configuration settings for the barcode decoding process.

## Example

```json
{
    "Section": "ST_BARCODE_DECODING",
    "ImageParameterName": "ip_dbrDefault",
    "StageArray": []
}
```

## Available Parameters

### Section

The name of the current section, whose value is a fixed value: `ST_BARCODE_DECODING`.

### ImageParameterName

Specifies the name of an `ImageParameter` object to apply in the stages of this section.

| Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>*It must be the name of an `ImageParameter` object defined under `ImageParameterOptions`* |
| **Default Value**<br>*""* |

### StageArray

`StageArray` is a parameter that specifies the stage objects within current section.

The `BarcodeDecodingSection` consists of following stages:

| Stage Name | Description |
|------------|-------------|
| [ResistDeformationStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-resist-deformation.html) | It defines the stage that applies preprocessing techniques to reduce image deformation and improve barcode recognition accuracy. |
| [ComplementBarcodeStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-complement-barcode.html) | It is designed at the stage level to define the configuration settings for the barcode complement process. |
| [ScaleBarcodeImageStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-scale-barcode-image.html) | It defines the stage where the barcode image is scaled according to the specified scaling mode to optimize recognition. |
| [DecodeBarcodesStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-decode-barcodes.html) | It defines the stage that extracts and interprets barcode data from the localized barcode regions). |
