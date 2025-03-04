---
layout: default-layout
title: Label Recognizer Task Setting - Dynamsoft Capture Vision Parameter File
description: Label Recognizer Task Setting object in the Dynamsoft Capture Vision Parameter File is an object for configuring and organizing the process of label recognition task.
keywords: label recognition, task, setting
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
---

# LabelRecognizerTaskSetting Object

The `LabelRecognizerTaskSetting` object is used to configure settings for a label recognition task to be performed on certain regions of interest (ROIs) in an image.

```json
{
    "Name": "dlr_task_default",
    "MaxThreadsInOneTask": 4,
    "TextLineSpecificationNameArray": [ "tls_default" ],
    "BaseLabelRecognizerTaskSettingName": "",
    "SectionArray": [
        {
            "Section": "ST_REGION_PREDETECTION",
            "ImageParameterName": "ip_default",
            "StageArray": [
                {
                    "Stage": "SST_PREDETECT_REGIONS",
                    "RegionPredetectionModes": [
                    ]
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
                    "StringLengthRange": [
                        3,
                        200
                    ],
                    "StringRegExPattern": ""
                }
            ]
            
        }
    ]
}
```

<div align="center">
   <p>Example 1 – Parameters of LabelRecognizerTaskSetting</p>
</div>

## Summary of LabelRecognizerTaskSetting top-level parameters

| Parameter Name | Description |
| -------------- | ----------- |
| [`Name`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/name.html) | Defines the name of a `LabelRecognizerTaskSetting` object, which serves as its unique identifier. |
| [`BaseLabelRecognizerTaskSettingName`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/base-label-recognizer-task-setting-name.html) | Represents the name of another `LabelRecognizerTaskSetting` object to inherit from. |
| [`MaxThreadsInOneTask`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/max-threads-in-one-task.html) | Defines the maximum threads that can be consumed in one task. |
| [`TextLineSpecificationNameArray`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/text-line-specification-name-array.html) | Defines the collection of text line specification object names. |
| [`SectionArray`]({{site.dcvb_parameters_reference}}label-recognizer-task-settings/section-array.html) | Defines which sections exist under the `LabelRecognizerTaskSetting`. |
