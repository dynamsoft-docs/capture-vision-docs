---
layout: default-layout
title: DocumentNormalizerTaskSetting - Dynamsoft Capture Vision Parameter File
description: The DocumentNormalizerTaskSetting object in the Dynamsoft Capture Vision Parameter File. 
needAutoGenerateSidebar: false
---

# DocumentNormalizerTaskSetting Object

The `DocumentNormalizerTaskSetting` object is used to configure settings for a document normalizer task to be performed on certain regions of interest (ROIs) in an image.

## Example

```json
{
    "Name": "ddn_task_default",
    "MaxThreadsInOneTask": 4,
    "ExpectedDocumentsCount": 1,
    "BaseDocumentNormalizerTaskSettingName": "",
    "SectionArray": [
        {
            "Section": "ST_REGION_PREDETECTION",
            "ImageParameterName": "ip_default",
            "StageArray": [
                {
                    "Stage": "SST_PREDETECT_REGIONS",
                    "RegionPredetectionModes": []
                }
            ]
        },
        {
            "Section": "ST_DOCUMENT_DETECTION",
            "ContentType": "CT_DOCUMENT",
            "ImageParameterName": "ip_default",
            "StageArray": [
                {
                    "Stage": "SST_ASSEMBLE_LONG_LINES"
                },
                {
                    "Stage": "SST_ASSEMBLE_LOGICAL_LINES"
                },
                {
                    "Stage": "SST_DETECT_CORNERS",
                    "CornerAngleRange": {
                        "MaxValue": 110,
                        "MinValue": 70
                    }
                },
                {
                    "Stage": "SST_DETECT_EDGES"
                },
                {
                    "Stage": "SST_DETECT_QUADS",
                    "QuadrilateralDetectionModes": [
                        {
                            "Mode": "QDM_GENERAL"
                        }
                    ]
                }
            ]
        },
        {
            "Section": "ST_DOCUMENT_DESKEWING",
            "ImageParameterName": "ip_default",
            "StageArray": [
                {
                    "Stage": "SST_DESKEW_IMAGE",
                    "DeskewMode": {
                        "ContentDirection": 0,
                        "Mode": "DSM_PERSPECTIVE_CORRECTION"
                    },
                    "PageSize": [-1, -1]
                }
            ]
        },
        {
            "Section": "ST_IMAGE_ENHANCEMENT",
            "ImageParameterName": "ip_0",
            "StageArray": [
                {
                    "Stage": "SST_ENHANCE_IMAGE",
                    "ColourMode": "ICM_COLOUR",
                    "Brightness": 0,
                    "Contrast": 0
                }
            ]
        }
    ]
}
```

## Parameters

| Parameter Name | Type | Required/Optional | Description |
| -------------- | ---- | ----------------- | ----------- |
| [`Name`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/name.html) | String | Required | The unique identifier for this `DocumentNormalizerTaskSetting` object. |
| [`BaseDocumentNormalizerTaskSettingName`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/base-document-normalizer-task-setting-name.html) | String | Optional | The name of another `DocumentNormalizerTaskSetting` object to inherit settings from. |
| [`MaxThreadsInOneTask`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/max-threads-in-one-task.html) | Integer | Optional | The maximum number of threads that can be used for this task. |
| [`ExpectedDocumentsCount`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/expected-documents-count.html) | Integer | Optional | The expected number of documents to be detected in the image. |
| [`SectionArray`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/section-array.html) | Array | Optional | An array of section objects that define the processing workflow for document normalization. |
