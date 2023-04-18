---
layout: default-layout
title: Barcode Reader Task Setting - Dynamsoft Capture Vision Parameter File
description: Barcode Reader Task Setting object in the Dynamsoft Capture Vision Parameter File is an object for configuring and organizing the process of barcode reading task.
keywords: barcode reader,task, setting
needAutoGenerateSidebar: false
---

# Barcode Reader Task Setting
In Dynamsoft Capture Vision(DCV), we use Json files to configure and organize the process tasks. The Barcode Reader Task Setting described in this chapter is one of the configurable tasks. If you have more strict requirements for speed or accuracy, it is highly recommended that you start by trying the barcode  reader task settings.

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

When DCV executes tasks related to barcode reading, it will process them according to the settings in the `BarcodeReaderTaskSetting`. For example, if you set BarcodeFormatIds = oneD, this Barcode reading task will not recognize barcode formats other than oneD.

## Barcode Reader Task Setting Example

```json
 {
    "Name": "BR_0",
    "MaxThreadsInOneTask":4, 
    "ExpectedBarcodesCount" : 512,
    "BarcodeFormatIds" : [ "BF_ALL" ],
    "DeblurLevel" : 9,
    "DeblurModes" : null,
    "BarcodeFormatSpecificationNameArray" : null,
    "LocalizationModes" : [
        {
            "LibraryFileName" : "",
            "LibraryParameters" : "",
            "Mode" : "LM_CONNECTED_BLOCKS"
        },
        {
            "LibraryFileName" : "",
            "LibraryParameters" : "",
            "Mode" : "LM_SCAN_DIRECTLY",
            "ScanDirection" : 0,
            "ScanStride" : 0
        },
        {
            "LibraryFileName" : "",
            "LibraryParameters" : "",
            "Mode" : "LM_STATISTICS"
        },
        {
            "LibraryFileName" : "",
            "LibraryParameters" : "",
            "Mode" : "LM_LINES"
        },
        {
            "LibraryFileName" : "",
            "LibraryParameters" : "",
            "Mode" : "LM_STATISTICS_MARKS"
        }
    ],
    "DPMCodeReadingModes" : [
        {
            "Mode" : "DPMCRM_SKIP"
        }
    ],
    "BarcodeColourModes" : [
         {
            "LibraryFileName" : "",
            "LibraryParameters" : "",
            "LightReflection" : 1,
            "Mode" : "BICM_DARK_ON_LIGHT"
         }
    ],
    "BarcodeComplementModes" : [
        {
            "Mode": "BCM_GENERAL" 
        }
    ],
    "DeformationResistingModes" : [
        {
            "Mode" : "DRM_SKIP"
        }
    ],

    "ResultCoordinateType" : "RCT_PIXEL",
    "ReturnBarcodeZoneClarity" : 0,
    "TextResultOrderModes" : [
        {
            "Mode" : "TROM_CONFIDENCE"
        },
        {
            "Mode" : "TROM_POSITION"
        },
        {
            "Mode" : "TROM_FORMAT"
        }
    ],    
    "SectionImageParameterArray":[
        {
            "Section": "REGION_PREDETECTION",
            "ImageParameterName": "IP_0"
        },
        {
            "Section": "BARCODE_LOCALIZATION",
            "ImageParameterName": "IP_1"
        },
        {
            "Section": "BARCODE_DECODING",
            "ImageParameterName": "IP_2"
        }
    ],
    "StartSection": "REGION_PREDETECTION", 
    "TerminateSetting": 
    {
        "Section": "REGION_PREDETECTION",
        "Stage": "IRUT_GRAYSCALE_IMAGE", 
    },
    "BaseBarcodeReaderTaskSettingName": "", 
}
```


## Other Tasks
Additional tasks other than barcode reading can be configured in the DCV template, as detailed in:

[DocumentNormalizerTaskSetting]()

[LabelRecognizerTaskSetting]()

For the DCV template, please read:

[Capture Vision Template]()

