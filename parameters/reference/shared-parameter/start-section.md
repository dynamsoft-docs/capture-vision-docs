---
layout: default-layout
Title: StartSection - Dynamsoft Capture Vision Shared Parameters
Description: The parameter StartSection defines the start section of the algorithm task.
Keywords: Max threads
needAutoGenerateSidebar: true
noTitleIndex: true
---

# StartSection

Parameter `StartSection` defines the start section of the algorithm task.

```json
{
    "StartSection": "ST_REGION_PREDETECTION"
}
```

> Note: Parameter `StartSection` is available for  `BarcodeReaderTaskSetting`, `LabelRecognizerTaskSetting` and `DocumentNormalizerTaskSetting`. They have different parameter range but the same default value.

## As a BarcodeReaderTaskSetting Parameter

| StartSection Parameter Details|
| :---------------------------- |
| **Type**<br>*string* |
| **Range**<li>ST_REGION_PREDETECTION</li><li>ST_BARCODE_LOCALIZATION</li><li>ST_BARCODE_DECODING</li> |
| **Default Value**<br>ST_REGION_PREDETECTION |

## As a DocumentNormalizerTaskSetting Parameter

| StartSection Parameter Details|
| :---------------------------- |
| **Type**<br>*string* |
| **Range**<li>ST_REGION_PREDETECTION</li><li>ST_DOCUMENT_DETECTION</li><li>ST_DOCUMENT_NORMALIZATION</li> |
| **Default Value**<br>ST_REGION_PREDETECTION |

## As a LabelRecognizerTaskSetting Parameter

| StartSection Parameter Details|
| :---------------------------- |
| **Type**<br>*string* |
| **Range**<li>ST_REGION_PREDETECTION</li><li>ST_TEXT_LINE_LOCALIZATION</li><li>ST_TEXT_LINE_RECOGNITION</li> |
| **Default Value**<br>ST_REGION_PREDETECTION |
