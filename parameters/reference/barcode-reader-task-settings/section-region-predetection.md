---
layout: default-layout
title: RegionPredetectionSection Object - Dynamsoft Barcode Reader Parameters
description: This page defines RegionPredetectionSection Object under the BarcodeReaderTaskSetting.
keywords: RegionPredetectionSection Object
---

# RegionPredetectionSection Object

The `RegionPredetectionSection` object is designed to identify region of interest (ROIs), allowing subsequent processing to ignore other parts of the image. The pre-detected region may be identified based on color features, grayscale features, or neural network localization.

## Example

```json
{
    "Section": "ST_REGION_PREDETECTION",
    "ImageParameterName": "ip_dbrDefault",
    "StageArray": []
}
```

## Available Parameters

### Section

The name of the current section, whose value is a fixed value: `ST_REGION_PREDETECTION`.

### ImageParameterName

Specifies the name of an `ImageParameter` object to apply in the stages of this section.

| Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>*It must be the name of an `ImageParameter` object defined under `ImageParameterOptions`* |
| **Default Value**<br>*""* |

### StageArray

`StageArray` is a parameter that specifies the stage objects within current section.

The `RegionPredetectionSection` consists of following stages:

| Stage Name | Description |
|------------|-------------|
| [PredetectRegionsStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-predetect-regions.html) | It defines the stage that identifies potential barcode regions before the main detection process. |
