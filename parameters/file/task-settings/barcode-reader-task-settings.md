---
layout: default-layout
title: Barcode Reader Task Setting - Dynamsoft Capture Vision Parameter File
description: Barcode Reader Task Setting object in the Dynamsoft Capture Vision Parameter File is an object for configuring and organizing the process of barcode reading task.
keywords: barcode reader,task, setting
needAutoGenerateSidebar: false
---

# BarcodeReaderTaskSetting Object

The `BarcodeReaderTaskSetting` object configures the barcode reading process in Dynamsoft Capture Vision (DCV). Use this object to optimize speed or accuracy for your specific barcode reading requirements.

## Example

```json
{
    "Name": "BR_0",
    "MaxThreadsInOneTask": 4,
    "ExpectedBarcodesCount": 512,
    "BarcodeFormatIds": ["BF_ALL"],
    "BarcodeFormatSpecificationNameArray": null,
    "DPMCodeReadingModes": [
        {
            "Mode": "DPMCRM_SKIP"
        }
    ],
    "SectionArray": [
        {
            "Section": "ST_REGION_PREDETECTION",
            "ImageParameterName": "ip_dbrDefault",
            "StageArray": [
                {
                    "Stage": "SST_PREDETECT_REGIONS",
                    "RegionPredetectionModes": []
                }
            ]
        },
        {
            "Section": "ST_BARCODE_LOCALIZATION",
            "ImageParameterName": "ip_dbrDefault",
            "StageArray": [
                {
                    "Stage": "SST_LOCALIZE_CANDIDATE_BARCODES",
                    "LocalizationModes": []
                },
                {
                    "Stage": "SST_LOCALIZE_BARCODES"
                }
            ]
        },
        {
            "Section": "ST_BARCODE_DECODING",
            "ImageParameterName": "ip_dbrDefault",
            "StageArray": [
                {
                    "Stage": "SST_COMPLEMENT_BARCODE",
                    "BarcodeComplementModes": []
                },
                {
                    "Stage": "SST_RESIST_DEFORMATION",
                    "DeformationResistingModes": []
                },
                {
                    "Stage": "SST_SCALE_BARCODE_IMAGE",
                    "BarcodeScaleModes": []
                },
                {
                    "Stage": "SST_DECODE_BARCODES",
                    "DeblurModes": [],
                    "ReturnBarcodeZoneClarity": 0
                }
            ]
        }
    ],
    "TextResultOrderModes": [
        {
            "Mode": "TROM_CONFIDENCE"
        }
    ],
    "BaseBarcodeReaderTaskSettingName": ""
}
```

## Parameters

| Parameter Name | Type | Required/Optional | Description |
| -------------- | ---- | ----------------- | ----------- |
| [`Name`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/name.html) | String | Required | The unique identifier for this `BarcodeReaderTaskSetting` object. |
| [`BarcodeFormatIds`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/barcode-format-ids.html) | String Array | Optional | Specifies which barcode formats to read. |
| [`BarcodeFormatSpecificationNameArray`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/barcode-format-specification-name-array.html) | String Array | Optional | Names of referenced `BarcodeFormatSpecification` objects for format-specific settings. |
| [`ExpectedBarcodesCount`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/expected-barcodes-count.html) | Integer | Optional | Expected number of barcodes to detect per image. |
| [`MaxThreadsInOneTask`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/max-threads-in-one-task.html) | Integer | Optional | Maximum number of parallel threads for this task. |
| [`SectionArray`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/section-array.html) | Object Array | Optional | Defines processing sections (region predetection, localization, decoding) and their stages. |
| [`DPMCodeReadingModes`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/dpm-code-reading-modes.html) | Object Array | Optional | Modes and priority for reading Direct Part Mark (DPM) codes. |
| [`TextResultOrderModes`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/text-result-order-modes.html) | Object Array | Optional | Order in which barcode results are returned. |
| [`BaseBarcodeReaderTaskSettingName`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/base-barcode-reader-task-setting-name.html) | String | Optional | Name of another `BarcodeReaderTaskSetting` object to inherit parameters from. |
