---
layout: default-layout
title: LabelRecognizerTaskSetting - Dynamsoft Capture Vision Parameter File
description: The LabelRecognizerTaskSetting object in the Dynamsoft Capture Vision Parameter File. 
keywords: label recognition, task, setting
needAutoGenerateSidebar: false
---

# LabelRecognizerTaskSetting Object

The `LabelRecognizerTaskSetting` object is used to configure settings for a label recognition task to be performed on certain regions of interest (ROIs) in an image.

## Example

```json
{
    "Name": "dlr_task_default",
    "MaxThreadsInOneTask": 4,
    "TextLineSpecificationNameArray": ["tls_default"],
    "BaseLabelRecognizerTaskSettingName": "",
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
            "Section": "ST_TEXT_LINE_LOCALIZATION",
            "ImageParameterName": "ip_default",
            "StageArray": [
                {
                    "Stage": "SST_LOCALIZE_TEXT_LINES"
                }
            ]
        },
        {
            "Section": "ST_TEXT_LINE_RECOGNITION",
            "ImageParameterName": "ip_default",
            "StageArray": [
                {
                    "Stage": "SST_RECOGNIZE_RAW_TEXT_LINES",
                    "DictionaryPath": "",
                    "DictionaryCorrectionThresholds": [
                        {
                            "MaxWordLength": 256,
                            "MinWordLength": 3,
                            "Threshold": 1
                        }
                    ],
                    "ConfusableCharactersPath": "ConfusableChars.data",
                    "ClusterSamplesCountThreshold": 0,
                    "OverlappingCharactersPath": "OverlappingChars.data",
                    "EnableRegexForceCorrection": 1
                },
                {
                    "Stage": "SST_ASSEMBLE_TEXT_LINES",
                    "StringLengthRange": [3, 200],
                    "StringRegExPattern": ""
                }
            ]
        }
    ]
}
```

## Parameters

| Parameter Name | Type | Required/Optional | Description |
| -------------- | ---- | ----------------- | ----------- |
| [`Name`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/name.html) | String | Required | The unique identifier for this `LabelRecognizerTaskSetting` object. |
| [`BaseLabelRecognizerTaskSettingName`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/base-label-recognizer-task-setting-name.html) | String | Optional | The name of another `LabelRecognizerTaskSetting` object to inherit settings from. |
| [`MaxThreadsInOneTask`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/max-threads-in-one-task.html) | Integer | Optional | The maximum number of threads that can be used for this task. |
| [`TextLineSpecificationNameArray`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/text-line-specification-name-array.html) | String Array | Optional | An array of text line specification object names that define how to recognize text lines. |
| [`SectionArray`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/section-array.html) | Array | Optional | An array of section objects that define the processing workflow for label recognition. |
