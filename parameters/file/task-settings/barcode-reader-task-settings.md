---
layout: default-layout
title: Barcode Reader Task Setting - Dynamsoft Capture Vision Parameter File
description: Barcode Reader Task Setting object in the Dynamsoft Capture Vision Parameter File is an object for configuring and organizing the process of barcode reading task.
keywords: barcode reader,task, setting
needAutoGenerateSidebar: false
---

# BarcodeReaderTaskSetting Object

In Dynamsoft Capture Vision(DCV), we use Json files to configure and organize the process tasks. The `BarcodeReaderTaskSetting` described in this chapter is one of the configurable tasks. If you have more strict requirements for speed or accuracy, it is highly recommended that you start by trying the barcode reader task settings.


## Available Settings

All available parameters related to barcode decoding are listed here, along with a brief description.

 | Parameter Name | Description |
 | -------------- | ----------- |
 | [`BarcodeFormatIds`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/barcode-format-ids.html) | Sets which barcode format the current FormatSpecification configuration is applied to. |
 | [`BarcodeFormatSpecificationNameArray`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/barcode-format-specification-name-array.html) | The names of the referenced BarcodeFormatSpecification object(s). |
 | [`DPMCodeReadingModes`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/dpm-code-reading-modes.html) | Sets the mode and priority for DPM code reading. |
 | [`ExpectedBarcodesCount`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/expected-barcodes-count.html) | Sets the number of barcodes expected to be detected for each image. |
 | [`MaxThreadsInOneTask`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/max-threads-in-one-task.html) | Represents the maximum number of parallel threads that can be used on a single task.|
 | [`Name`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/name.html) | The name of the BarcodeReaderTaskSetting object. |
 | [`SectionArray`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-array.html) | Defines which sections exist under the `BarcodeReaderTaskSetting`. |
 | [`TextResultOrderModes`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/text-result-order-modes.html) | Sets the mode and priority for the order of the text results returned. |
 | [`BaseBarcodeReaderTaskSettingName`]({{site.dcvb_parameters_reference}}barcode-reader-task-settings/base-barcode-reader-task-setting-name.html) | Sets the name of a BarcodeReaderTaskSetting object to be Inheritanced.|

When DCV executes tasks related to barcode reading, it will process them according to the settings in the `BarcodeReaderTaskSetting`. Here is a sample:

## Barcode Reader Task Setting Example

```json
 {
    "Name": "BR_0",
    "MaxThreadsInOneTask":4, 
    "ExpectedBarcodesCount" : 512,
    "BarcodeFormatIds" : [ "BF_ALL" ],
    "BarcodeFormatSpecificationNameArray" : null,
    "DPMCodeReadingModes" : [
        {
            "Mode" : "DPMCRM_SKIP"
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
                    "ReturnBarcodeZoneClarity" : 0
                }
            ]
        }
    ],
    "TextResultOrderModes" : [
        {
            "Mode" : "TROM_CONFIDENCE"
        }
    ],
    "BaseBarcodeReaderTaskSettingName": ""
}
```
