---
layout: default-layout
Title: StartSection - Dynamsoft Capture Vision Shared Parameters
Description: The parameter StartSection defines the start section of the algorithm task.
Keywords: Start section
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/shared-parameter/start-section.html
---

# StartSection

Parameter `StartSection` defines the start section of the algorithm task.

## Example

```json
{
    "StartSection": "ST_REGION_PREDETECTION"
}
```

## Parameter Summary

Parameter `StartSection` is available for  `BarcodeReaderTaskSetting`, `LabelRecognizerTaskSetting` and `DocumentNormalizerTaskSetting`. It has different parameter range but the same default value under different parent object.

### As a BarcodeReaderTaskSetting Parameter

| StartSection Parameter Summary |
| :---------------------------- |
| **Type**<br>*string* |
| **Range**<br>ST_REGION_PREDETECTION<br>ST_BARCODE_LOCALIZATION<br>ST_BARCODE_DECODING |
| **Default Value**<br>ST_REGION_PREDETECTION |

### As a DocumentNormalizerTaskSetting Parameter

| StartSection Parameter Summary |
| :---------------------------- |
| **Type**<br>*string* |
| **Range**<br>ST_REGION_PREDETECTION<br>ST_DOCUMENT_DETECTION<br>ST_DOCUMENT_NORMALIZATION |
| **Default Value**<br>ST_REGION_PREDETECTION |

### As a LabelRecognizerTaskSetting Parameter

| StartSection Parameter Summary |
| :---------------------------- |
| **Type**<br>*string* |
| **Range**<br>ST_REGION_PREDETECTION<br>ST_TEXT_LINE_LOCALIZATION<br>ST_TEXT_LINE_RECOGNITION |
| **Default Value**<br>ST_REGION_PREDETECTION |
