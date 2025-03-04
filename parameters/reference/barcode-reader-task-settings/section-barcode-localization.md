---
layout: default-layout
title: BarcodeLocalizationSection Object - Dynamsoft Barcode Reader Parameters
description: This page defines BarcodeLocalizationSection Object under the BarcodeReaderTaskSetting.
keywords: BarcodeLocalizationSection Object
---

# BarcodeLocalizationSection Object

The `BarcodeLocalizationSection` object is designed to define the configuration settings for the barcode localization process. 

## Example

```json
{
    "Section": "ST_BARCODE_LOCALIZATION",
    "ImageParameterName": "ip_dbrDefault",
    "StageArray": []
}
```

## Available Parameters

### Section

The name of the current section, whose value is a fixed value: `ST_BARCODE_LOCALIZATION`.

### ImageParameterName

Specifies the name of an `ImageParameter` object to apply in the stages of this section.

| Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>*It must be the name of an `ImageParameter` object defined under `ImageParameterOptions`* |
| **Default Value**<br>*""* |

### StageArray

`StageArray` is a parameter that specifies the stage objects within current section.

The `BarcodeLocalizationSection` consists of following stages:

| Stage Name | Description |
|------------|-------------|
| [LocalizeCandidateBarcodesStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-localize-candidate-barcodes.html) | It defines the stage that detects and marks potential barcode locations within the image for further processing. |
| [LocalizeBarcodesStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-localize-barcodes.html) | It defines the stage that accurately determines the positions of barcodes within the identified candidate regions. |
