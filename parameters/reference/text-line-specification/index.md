---
layout: default-layout
title: TextLineSpecification Parameters - Dynamsoft Capture Vision
description: Reference index for TextLineSpecification object in Dynamsoft Capture Vision parameters, which define configurations for specified text lines including character models, regex patterns, and recognition settings.
keywords: TextLineSpecification, text line, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# TextLineSpecification Parameters

The `TextLineSpecification` object defines configurations for specified text lines, including character models, recognition patterns, and output settings.

## Example JSON

```json
{
    "TextLineSpecificationOptions": [
        {
            "Name": "tls_default",
            "BaseTextLineSpecificationName": "",
            "ApplicableTextLineNumbers": [0],
            "CharacterModelName": "",
            "TextLineRecModelName": "",
            "CharHeightRange": [5, 1000],
            "CharacterNormalizationModes": [],
            "BinarizationModes": [],
            "GrayscaleEnhancementModes": [],
            "StringLengthRange": [3, 200],
            "StringRegexPattern": "",
            "OutputResults": 1,
            "ConcatResults": 0,
            "ConcatSeparator": "",
            "ConcatStringLengthRange": [0, 0],
            "ConcatStringRegexPattern": "",
            "ExpectedGroupsCount": 1,
            "SubGroups": [],
            "ReferenceGroupName": "",
            "TextLinesCount": 1,
            "Position": { "Left": -1, "Top": -1, "Right": -1, "Bottom": -1 },
            "ConfusableCharactersCorrection": {
                "ConfusionSet": "",
                "FontName": "",
                "Height": 0,
                "Width": 0
            }
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `TextLineSpecification` object inside `TextLineSpecificationOptions`.

```text
TextLineSpecification
├── Name
├── BaseTextLineSpecificationName
├── ApplicableTextLineNumbers
├── CharacterModelName
├── TextLineRecModelName
├── CharHeightRange
├── CharacterNormalizationModes
├── BinarizationModes
├── GrayscaleEnhancementModes
├── StringLengthRange
├── StringRegexPattern
├── OutputResults
├── ConcatResults
├── ConcatSeparator
├── ConcatStringLengthRange
├── ConcatStringRegexPattern
├── ExpectedGroupsCount
├── SubGroups
├── ReferenceGroupName
├── TextLinesCount
├── Position
└── ConfusableCharactersCorrection
```

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the TextLineSpecification object. |
| [`BaseTextLineSpecificationName`](base-text-line-specification-name.md) | The name of another TextLineSpecification to inherit from. |
| [`ApplicableTextLineNumbers`](applicable-text-line-numbers.md) | The text line numbers this specification applies to. |
| [`CharacterModelName`](character-model-name.md) | The name of the character recognition model. |
| [`TextLineRecModelName`](text-line-rec-model-name.md) | The name of the text line recognition model. |
| [`CharHeightRange`](char-height-range.md) | The expected character height range. |
| [`CharacterNormalizationModes`](character-normalization-modes.md) | The modes for character normalization. |
| [`BinarizationModes`](binarization-modes.md) | The modes for binarization. |
| [`GrayscaleEnhancementModes`](grayscale-enhancement-modes.md) | The modes for grayscale enhancement. |
| [`StringLengthRange`](string-length-range.md) | The expected string length range. |
| [`StringRegexPattern`](string-regex-pattern.md) | The regex pattern for validating recognized strings. |
| [`OutputResults`](output-results.md) | Whether to output results for this specification. |
| [`ConcatResults`](concat-results.md) | Whether to concatenate results. |
| [`ConcatSeparator`](concat-separator.md) | The separator for concatenated results. |
| [`ConcatStringLengthRange`](concat-string-length-range.md) | The length range for concatenated strings. |
| [`ConcatStringRegexPattern`](concat-string-regex-pattern.md) | The regex pattern for concatenated strings. |
| [`ExpectedGroupsCount`](expected-groups-count.md) | The expected number of text line groups. |
| [`SubGroups`](sub-groups.md) | The sub-group definitions. |
| [`ReferenceGroupName`](reference-group-name.md) | The name of the reference group. |
| [`TextLinesCount`](text-lines-count.md) | The expected number of text lines. |
| [`Position`](position.md) | The position of the text line. |
| [`ConfusableCharactersCorrection`](confusable-characters-correction.md) | The settings for confusable characters correction. |


