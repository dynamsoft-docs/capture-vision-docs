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
| **Range**<br>* ST_REGION_PREDETECTION<br>* ST_BARCODE_LOCALIZATION<br>* ST_BARCODE_DECODING |
| **Default Value**<br>ST_REGION_PREDETECTION |

## As a DocumentNormalizerTaskSetting Parameter

| StartSection Parameter Details|
| :---------------------------- |
| **Type**<br>*string* |
| **Range**<br>* ST_REGION_PREDETECTION<br>* ST_DOCUMENT_DETECTION<br>* ST_DOCUMENT_NORMALIZATION |
| **Default Value**<br>ST_REGION_PREDETECTION |

## As a LabelRecognizerTaskSetting Parameter

| StartSection Parameter Details|
| :---------------------------- |
| **Type**<br>*string* |
| **Range**<br>* ST_REGION_PREDETECTION<br>* ST_TEXT_LINE_LOCALIZATION<br>* ST_TEXT_LINE_RECOGNITION |
| **Default Value**<br>ST_REGION_PREDETECTION |
