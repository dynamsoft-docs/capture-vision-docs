---
layout: default-layout
title: LabelRecognizerTaskSetting Parameters - Dynamsoft Capture Vision
description: Reference index for LabelRecognizerTaskSetting parameters in Dynamsoft Capture Vision, including text line localization, recognition, dictionary correction, and confusable characters settings.
keywords: LabelRecognizerTaskSetting, label recognizer, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# LabelRecognizerTaskSetting Parameters

The `LabelRecognizerTaskSetting` object configures settings for label recognition tasks in Dynamsoft Capture Vision, including text line localization, recognition, and correction.

## General

| Parameter | Description |
|:----------|:------------|
| [`Name`](name.html) | The unique name of the LabelRecognizerTaskSetting object. |
| [`BaseLabelRecognizerTaskSettingName`](base-label-recognizer-task-setting-name.html) | The name of another LabelRecognizerTaskSetting to inherit from. |
| [`MaxThreadsInOneTask`](max-threads-in-one-task.html) | The maximum threads in one task. |

## Text Recognition Settings

| Parameter | Description |
|:----------|:------------|
| [`TextLineSpecificationNameArray`](text-line-specification-name-array.html) | The names of TextLineSpecification objects to reference. |
| [`StringLengthRange`](string-length-range.html) | The expected string length range. |
| [`StringRegexPattern`](string-regex-pattern.html) | The regex pattern for validating recognized strings. |
| [`DictionaryPath`](dictionary-path.html) | The path to the dictionary file. |
| [`DictionaryCorrectionThresholds`](dictionary-correction-thresholds.html) | The thresholds for dictionary-based correction. |
| [`ConfusableCharactersPath`](confusable-characters-path.html) | The path to confusable characters definition. |
| [`OverlappingCharactersPath`](overlapping-characters-path.html) | The path to overlapping characters definition. |
| [`ClusterSamplesCountThreshold`](cluster-samples-count-threshold.html) | The threshold for cluster samples count. |
| [`EnableRegexForceCorrection`](enable-regex-force-correction.html) | Whether to enable regex-based force correction. |

## Processing Modes

| Parameter | Description |
|:----------|:------------|
| [`LocalizationModes`](localization-modes.html) | The modes for text line localization. |
| [`OrientationDetectionModes`](orientation-detection-modes.html) | The modes for orientation detection. |

## Section & Stage Configuration

| Parameter | Description |
|:----------|:------------|
| [`SectionArray`](section-array.html) | The sections of the label recognizer task. |
| [`SectionRegionsPredetection`](section-regions-predetection.html) | Region predetection section settings. |
| [`SectionTextLinesLocalization`](section-text-lines-localization.html) | Text line localization section settings. |
| [`SectionTextLinesRecognition`](section-text-lines-recognition.html) | Text line recognition section settings. |
| [`StagePredetectRegions`](stage-predetect-regions.html) | Stage for predetecting regions. |
| [`StageLocalizeTextLines`](stage-localize-text-lines.html) | Stage for localizing text lines. |
| [`StageAssembleTextLines`](stage-assemble-text-lines.html) | Stage for assembling text lines. |
| [`StageRecognizeRawTextLines`](stage-recognize-raw-text-lines.html) | Stage for recognizing raw text lines. |
