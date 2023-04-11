---
title: Dynamsoft Capture Vision Barcode Reader Task Setting
description: Dynamsoft Capture Vision Barcode Reader Task Setting
keywords: barcode reader,task, setting
needAutoGenerateSidebar: false
permalink: N/A
---

# Barcode Reader Task Setting
In Dynamsoft Capture Vision(DCV), we use Json files to configure and organize the process tasks. the Barcode Reader Task Setting described in this chapter is one of the configurable tasks, and it is recommended that you read this article if you want the program to be better adapted to your business scenario.

Control reference content.
 | Parameter Name | Description |
 | -------------- | ----------- | 
 | [`BarcodeReaderTaskSetting.Name`](#name) | The name of the BarcodeReaderTaskSetting object. |
 | [`BarcodeReaderTaskSetting.Description`](#description) | The description of the ImageParameter object. |
 | [`BarcodeReaderTaskSetting.FormatSpecificationNameArray`](#formatspecificationnamearray) | The names of the referenced FormatSpecification object(s). |



## Available Settings
All available parameters related to barcode decoding are listed here, along with a brief description.

 | Parameter Name | Description |
 | -------------- | ----------- |
 | [`ExpectedBarcodesCount`]() |  |
 | [`BarcodeFormatIds`]() |  |
 | [`DeblurLevel`]() |  |
 | [`DeblurModes`]() |  |
 | [`LocalizationModes`]() |  |
 | [`DPMCodeReadingModes`]() |  |
 | [`BarcodeColourModes`]() |  |
 | [`BarcodeComplementModes`]() |  |
 | [`DeformationResistingModes`]() |  |
 | [`ResultCoordinateType`]() |  |
 | [`ReturnBarcodeZoneClarity`]() |  |
 | [`TextResultOrderModes`]() |  |
 | [`BaseBarcodeReaderTaskSettingName`]() |  |

BarcodeReaderTaskSettingOptions object
## Barcode Reader Task JSON Parameter Example

```json
 "BarcodeReaderTaskSettingOptions": [
        {
            "Name": "BR_0",
            "ExpectedBarcodesCount": 512,
            "BarcodeFormatIds": [
                "BF_ONED"
            ],
            "BarcodeFormatIds_2": [
				"BF2_NULL"
			],
            "DeblurLevel": 9,
            "DeblurModes": null,
            "BarcodeFormatSpecificationNameArray": ["FS_0"],
            "SectionImageParameterArray": [
                {
                    "Section": "REGION_PREDETECTION",
                    "ImageParameterName": "IP_0"
                },
                {
                    "Section": "BARCODE_LOCALIZATION",
                    "ImageParameterName": "IP_0"
                },
                {
                    "Section": "BARCODE_DECODING",
                    "ImageParameterName": "IP_0"
                }
            ],
            "StartSection": "REGION_PREDETECTION",
            "BaseBarcodeReaderTaskSettingName": ""
        }
    ],
```


## Other Tasks
在DCV模板中还可以配置其他类型的任务，详见：
[DocumentNormalizerTaskSetting]()
[LabelRecognizerTaskSetting]()
关于DCV模板，请阅读：
[Capture Vision Template]()

