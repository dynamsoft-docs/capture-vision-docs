---
layout: default-layout
title: DocumentNormalizerTaskSetting - Dynamsoft Capture Vision Parameter File
description: The DocumentNormalizerTaskSetting object in the Dynamsoft Capture Vision Parameter File. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /parameters/file/task-settings/document-normalizer-task-settings.html
---

# DocumentNormalizerTaskSetting Object

## Parameter Organization

A `DocumentNormalizerTaskSetting` object is defined as below:

| Key Name | Value Type | Required or Optional | Description |
|---|---|---|---|
| Name | string | Mandatory | Sets the name of current `DocumentNormalizerTaskSetting` object. The value must be unique between all `task-setting` objects. |
| Brightness | string | Optional | Sets the value for parameter [Brightness]({{site.parameterReference}}brightness.html) |
| ColourMode | string | Optional | Sets the value for parameter [ColourMode]({{site.parameterReference}}colour-mode.html) |
| ContentType | string | Optional | Sets the value for parameter [ContentType]({{site.parameterReference}}content-type.html) |
| Contrast | string | Optional | Sets the value for parameter [Contrast]({{site.parameterReference}}contrast.html) |
| CornerAngleRangeArray | string | Optional | Sets the value for parameter [CornerAngleRangeArray]({{site.parameterReference}}corner-angle-range-array.html) |
| DeskewMode | string | Optional | Sets the value for parameter [DeskewMode]({{site.parameterReference}}deskew-mode.html) |
| LineExtractionModes | string | Optional | Sets the value for parameter [LineExtractionModes]({{site.parameterReference}}line-extraction-modes.html) |
| MaxThreadsInOneTask | string array | Optional | Sets the value for parameter [MaxThreadsInOneTask]({{site.parameterReference}}max-threads-in-one-task.html) |
| PageSize | string | Optional | Sets the value for parameter [PageSize]({{site.parameterReference}}page-size.html) |
| QuadrilateralDetectionModes | string | Optional | Sets the value for parameter [QuadrilateralDetectionModes]({{site.parameterReference}}quadrilateral-detection-modes.html) |
| SectionImageParameterArray | string | Optional | Sets the value for parameter [SectionImageParameterArray]({{site.parameterReference}}section-image-parameter-array.html) |
| StartSection | string | Optional | Sets the value for parameter [StartSection]({{site.parameterReference}}start-section.html) |
| TerminateSetting | string | Optional | Sets the value for parameter [TerminateSetting]({{site.parameterReference}}terminate-setting.html) |
| BaseDocumentNormalizerTaskSettingName | string | Optional | Sets the value for parameter [BaseDocumentNormalizerTaskSettingName]({{site.parameterReference}}base-document-normalizer-task-setting-name.html) |

Here is a sample:

```JSON
{
    "Name": "DR_1",
    "MaxThreadsInOneTask":4,
    "LineExtractionModes" : [
        {
            "Mode": "LEM_GENERAL"
        }
    ],
    "Brightness" : 0,
    "ColourMode" : "ICM_COLOUR",
    "ContentType" : "CT_DOCUMENT",
    "Contrast" : 0,
    "DeskewMode" : 
    {
        "ContentDirection" : 0,
        "Mode" : "DM_PERSPECTIVE_CORRECTION"
    },
    "CornerAngleRangeArray" : [
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
