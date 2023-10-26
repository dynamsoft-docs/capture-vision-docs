---
layout: default-layout
title: Barcode Reader Task Setting - Dynamsoft Capture Vision Parameter File
description: Barcode Reader Task Setting object in the Dynamsoft Capture Vision Parameter File is an object for configuring and organizing the process of barcode reading task.
keywords: barcode reader,task, setting
needAutoGenerateSidebar: false
permalink: /parameters/file/task-settings/barcode-reader-task-settings.html
---

# Barcode Reader Task Setting
In Dynamsoft Capture Vision(DCV), we use Json files to configure and organize the process tasks. The Barcode Reader Task Setting described in this chapter is one of the configurable tasks. If you have more strict requirements for speed or accuracy, it is highly recommended that you start by trying the barcode  reader task settings.

Control reference content.

 | Parameter Name | Description |
 | -------------- | ----------- | 
 | [`BarcodeReaderTaskSetting.Name`]({{site.dcv_parameters_reference}}shared-parameter/name.html) | The name of the BarcodeReaderTaskSetting object. |
 | [`BarcodeReaderTaskSetting.BarcodeFormatSpecificationNameArray`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/barcode-format-specification-name-array.html) | The names of the referenced BarcodeFormatSpecification object(s). |



## Available Settings
All available parameters related to barcode decoding are listed here, along with a brief description.

 | Parameter Name | Description |
 | -------------- | ----------- |
 | [`ExpectedBarcodesCount`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/expected-barcodes-count.html) | Sets the number of barcodes expected to be detected for each image. |
 | [`BarcodeFormatIds`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/barcode-format-ids.html) | Sets which barcode format the current FormatSpecification configuration is applied to. |
 | [`DeblurModes`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/deblur-modes.html) | Sets the mode and priority for deblurring. |
 | [`LocalizationModes`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/localization-modes.html) | Sets the mode and priority for barcode localization algorithms. |
 | [`DPMCodeReadingModes`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/dpm-code-reading-modes.html) | Sets the mode and priority for DPM code reading. |
 | [`BarcodeColourModes`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/barcode-colour-modes.html) | Sets the mode and priority for the barcode colour mode used to process the barcode zone. |
 | [`BarcodeComplementModes`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/barcode-complement-modes.html) | Sets the mode and priority to complement the missing parts in the barcode. |
 | [`DeformationResistingModes`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/deformation-resisting-modes.html) | Sets the mode and priority for deformation resisting. |
 | [`ReturnBarcodeZoneClarity`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/return-barcode-zone-clarity.html) | Sets whether or not to return the clarity of the barcode zone. |
 | [`TextResultOrderModes`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/text-result-order-modes.html) | Sets the mode and priority for the order of the text results returned. |
 | [`BaseBarcodeReaderTaskSettingName`]({{site.dcv_parameters_reference}}barcode-reader-task-settings/base-barcode-reader-task-setting-name.html) | Sets the name of a BarcodeReaderTaskSetting object to be Inheritanced.|
| [`SectionImageParameterArray`]({{site.dcv_parameters_reference}}shared-parameter/section-image-parameter-array.html) | Sets image parameters for three different sections, where each section performs image processing stages with different parameters.|
| [`StartSection`]({{site.dcv_parameters_reference}}shared-parameter/start-section.html) | Indicates which Section the task will start executing from.|
| [`TerminateSetting`]({{site.dcv_parameters_reference}}shared-parameter/terminate-setting.html) | Indicates where the task stops, specifically indicating a Stage under a certain Section.|
| [`MaxThreadsInOneTask`]({{site.dcv_parameters_reference}}shared-parameter/max-threads-in-one-task.html) | Represents the maximum number of parallel threads that can be used on a single task.|

When DCV executes tasks related to barcode reading, it will process them according to the settings in the `BarcodeReaderTaskSetting`. Here is a sample:

## Barcode Reader Task Setting Example

```json
 {
    "Name": "BR_0",
    "MaxThreadsInOneTask":4, 
    "ExpectedBarcodesCount" : 512,
    "BarcodeFormatIds" : [ "BF_ALL" ],
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

