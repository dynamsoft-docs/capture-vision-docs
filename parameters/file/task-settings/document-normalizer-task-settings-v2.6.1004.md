---
layout: default-layout
title: DocumentNormalizerTaskSetting - Dynamsoft Capture Vision Parameter File
description: The DocumentNormalizerTaskSetting object in the Dynamsoft Capture Vision Parameter File. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
---

# DocumentNormalizerTaskSetting Object

## Parameter Organization

A `DocumentNormalizerTaskSetting` object is defined as below:

| Key Name | Value Type | Required or Optional | Description |
|---|---|---|---|
| Name | string | Mandatory | Sets the name of current `DocumentNormalizerTaskSetting` object. The value must be unique between all `task-setting` objects. |
| Brightness | string | Optional | Sets the value for parameter [Brightness]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/brightness.html) |
| ColourMode | string | Optional | Sets the value for parameter [ColourMode]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/colour-mode.html) |
| ContentType | string | Optional | Sets the value for parameter [ContentType]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/content-type.html) |
| Contrast | string | Optional | Sets the value for parameter [Contrast]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/contrast.html) |
| CornerAngleRange | string | Optional | Sets the value for parameter [CornerAngleRange]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/corner-angle-range.html) |
| DeskewMode | string | Optional | Sets the value for parameter [DeskewMode]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/deskew-mode.html) |
| ExpectedDocumentsCount | string | Optional | Sets the value for parameter [ExpectedDocumentsCount]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/expected-documents-count.html) |
| LineAssemblyMode | string | Optional | Sets the value for parameter [LineAssemblyMode]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/line-assembly-mode.html) |
| MaxThreadsInOneTask | string array | Optional | Sets the value for parameter [MaxThreadsInOneTask]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/max-threads-in-one-task.html) |
| PageSize | string | Optional | Sets the value for parameter [PageSize]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/page-size.html) |
| QuadrilateralDetectionModes | string | Optional | Sets the value for parameter [QuadrilateralDetectionModes]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/quadrilateral-detection-modes.html) |
| SectionImageParameterArray | string | Optional | Sets the value for parameter [SectionImageParameterArray]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/section-image-parameter-array.html) |
| ShortLineDetectionMode | string | Optional | Sets the value for parameter [ShortLineDetectionMode]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/short-line-detection-mode.html) |
| StartSection | string | Optional | Sets the value for parameter [StartSection]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/start-section.html) |
| TerminateSetting | string | Optional | Sets the value for parameter [TerminateSetting]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/terminate-setting.html) |
| BaseDocumentNormalizerTaskSettingName | string | Optional | Sets the value for parameter [BaseDocumentNormalizerTaskSettingName]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/base-document-normalizer-task-setting-name.html) |

Here is a sample:

```json
{
    "Name": "DR_1",
    "MaxThreadsInOneTask":4,
    "Brightness" : 0,
    "ColourMode" : "ICM_COLOUR",
    "ContentType" : "CT_DOCUMENT",
    "Contrast" : 0,
    "DeskewMode" : 
    {
        "ContentDirection" : 0,
        "Mode" : "DM_PERSPECTIVE_CORRECTION"
    },
    "CornerAngleRange" : [
        {
            "MaxValue" : 110,
            "MinValue" : 70
        }
    ],
    "PageSize" : [-1, -1],
    "QuadrilateralDetectionModes" : [
        {
            "Mode" : "QDM_GENERAL"
        }
    ],
    "LineAssemblyMode":
    {
        "Mode": "LAM_GENERAL",
        "Sensitivity": 3
    },
    "ShortlineDetectionMode":
    {
        "Mode": "SDM_GENERAL",
        "Sensitivity": 3
    }
    "SectionImageParameterArray" : [
        {
            "Section": "REGION_PREDETECTION",
            "ImageParameterName": "IP_0"
        },
        {
            "Section": "DOCUMENT_DETECTION",
            "ImageParameterName": "IP_1"
        },
        {
            "Section": "DOCUMENT_NORMALIZATION",
            "ImageParameterName": "IP_2"
        }
    ],
    "StartSection": "REGION_PREDETECTION",
    "TerminateSetting":
    {
        "Section": "REGION_PREDETECTION",
        "Stage": "IRUT_GRAYSCALE_IMAGE",
    },    
    "BaseDocumentNormalizerTaskSettingName": "",
}
```
