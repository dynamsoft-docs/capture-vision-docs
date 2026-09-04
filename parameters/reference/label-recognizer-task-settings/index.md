---
layout: default-layout
title: LabelRecognizerTaskSetting Parameters - Dynamsoft Capture Vision
description: Reference index for LabelRecognizerTaskSetting object in Dynamsoft Capture Vision parameters, including text line localization, recognition, dictionary correction, and confusable characters settings.
keywords: LabelRecognizerTaskSetting, label recognizer, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# LabelRecognizerTaskSetting Parameters

The `LabelRecognizerTaskSetting` object configures settings for label recognition tasks in Dynamsoft Capture Vision, including text line localization, recognition, and correction.

## Example JSON

```json
{
    "LabelRecognizerTaskSettingOptions": [
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
                            "Stage": "SST_LOCALIZE_TEXT_LINES",
                            "LocalizationModes": [],
                            "OrientationDetectionModes": []
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
                            "DictionaryCorrectionThresholds": [],
                            "ConfusableCharactersPath": "ConfusableChars.data",
                            "ClusterSamplesCountThreshold": 0,
                            "OverlappingCharactersPath": "OverlappingChars.data",
                            "EnableRegexForceCorrection": 1
                        },
                        {
                            "Stage": "SST_ASSEMBLE_TEXT_LINES",
                            "StringLengthRange": [3, 200],
                            "StringRegexPattern": ""
                        }
                    ]
                }
            ]
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `LabelRecognizerTaskSetting` object inside `LabelRecognizerTaskSettingOptions`.

```text
LabelRecognizerTaskSetting
├── Name
├── MaxThreadsInOneTask
├── TextLineSpecificationNameArray
├── BaseLabelRecognizerTaskSettingName
└── SectionArray[]
    ├── item (Section = ST_REGION_PREDETECTION)
    │   ├── Section
    │   ├── ImageParameterName
    │   └── StageArray[]
    │       └── item (Stage = SST_PREDETECT_REGIONS)
    │           ├── Stage
    │           └── RegionPredetectionModes
    ├── item (Section = ST_TEXT_LINE_LOCALIZATION)
    │   ├── Section
    │   ├── ImageParameterName
    │   └── StageArray[]
    │       └── item (Stage = SST_LOCALIZE_TEXT_LINES)
    │           ├── Stage
    │           ├── LocalizationModes
    │           └── OrientationDetectionModes
    └── item (Section = ST_TEXT_LINE_RECOGNITION)
        ├── Section
        ├── ImageParameterName
        └── StageArray[]
            ├── item (Stage = SST_RECOGNIZE_RAW_TEXT_LINES)
            │   ├── Stage
            │   ├── DictionaryPath
            │   ├── DictionaryCorrectionThresholds
            │   ├── ConfusableCharactersPath
            │   ├── ClusterSamplesCountThreshold
            │   ├── OverlappingCharactersPath
            │   └── EnableRegexForceCorrection
            └── item (Stage = SST_ASSEMBLE_TEXT_LINES)
                ├── Stage
                ├── StringLengthRange
                └── StringRegexPattern
```

> [!IMPORTANT]
> `Stage` values are constrained by the parent `Section` value, and stage-scoped parameters are constrained by the `Stage` value.

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the LabelRecognizerTaskSetting object. |
| [`BaseLabelRecognizerTaskSettingName`](base-label-recognizer-task-setting-name.md) | The name of another LabelRecognizerTaskSetting to inherit from. |
| [`MaxThreadsInOneTask`](max-threads-in-one-task.md) | The maximum threads in one task. |
| [`TextLineSpecificationNameArray`](text-line-specification-name-array.md) | The names of TextLineSpecification objects to reference. |
| [`SectionArray`](section-array.md) | The sections of the label recognizer task. |

## Nested Parameter Quick Links

### Actual Nested Parameters in the Tree

| Parameter Name | Description |
|:---------------|:------------|
| [`RegionPredetectionModes`](../image-parameter/region-predetection-modes.md) | Controls how to find a region of interest (ROI) within the image or frame. |
| [`LocalizationModes`](localization-modes.md) | The modes for text line localization. |
| [`OrientationDetectionModes`](orientation-detection-modes.md) | The modes for orientation detection. |
| [`DictionaryPath`](dictionary-path.md) | The path to the dictionary file. |
| [`DictionaryCorrectionThresholds`](dictionary-correction-thresholds.md) | The thresholds for dictionary-based correction. |
| [`ConfusableCharactersPath`](confusable-characters-path.md) | The path to confusable characters definition. |
| [`ClusterSamplesCountThreshold`](cluster-samples-count-threshold.md) | The threshold for cluster samples count. |
| [`OverlappingCharactersPath`](overlapping-characters-path.md) | The path to overlapping characters definition. |
| [`EnableRegexForceCorrection`](enable-regex-force-correction.md) | Whether to enable regex-based force correction. |
| [`StringLengthRange`](string-length-range.md) | The expected string length range. |
| [`StringRegexPattern`](string-regex-pattern.md) | The regex pattern for validating recognized strings. |

### Conceptual Section/Stage Objects

| Object | Description |
|:-------|:------------|
| [`SectionRegionsPredetection`](section-regions-predetection.md) | Section object for `Section = ST_REGION_PREDETECTION`. |
| [`StagePredetectRegions`](stage-predetect-regions.md) | Stage object under `Section = ST_REGION_PREDETECTION` with `Stage = SST_PREDETECT_REGIONS`. |
| [`SectionTextLinesLocalization`](section-text-lines-localization.md) | Section object for `Section = ST_TEXT_LINE_LOCALIZATION`. |
| [`StageLocalizeTextLines`](stage-localize-text-lines.md) | Stage object under `Section = ST_TEXT_LINE_LOCALIZATION` with `Stage = SST_LOCALIZE_TEXT_LINES`. |
| [`SectionTextLinesRecognition`](section-text-lines-recognition.md) | Section object for `Section = ST_TEXT_LINE_RECOGNITION`. |
| [`StageRecognizeRawTextLines`](stage-recognize-raw-text-lines.md) | Stage object under `Section = ST_TEXT_LINE_RECOGNITION` with `Stage = SST_RECOGNIZE_RAW_TEXT_LINES`. |
| [`StageAssembleTextLines`](stage-assemble-text-lines.md) | Stage object under `Section = ST_TEXT_LINE_RECOGNITION` with `Stage = SST_ASSEMBLE_TEXT_LINES`. |


