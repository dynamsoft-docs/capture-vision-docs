---
layout: default-layout
title: TextLineSpecification Parameters - Dynamsoft Capture Vision
description: Reference index for TextLineSpecification parameters in Dynamsoft Capture Vision, which define configurations for specified text lines including character models, regex patterns, and recognition settings.
keywords: TextLineSpecification, text line, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# TextLineSpecification Parameters

The `TextLineSpecification` object defines configurations for specified text lines, including character models, recognition patterns, and output settings.

## General

| Parameter | Description |
|:----------|:------------|
| [`Name`](name.html) | The unique name of the TextLineSpecification object. |
| [`BaseTextLineSpecificationName`](base-text-line-specification-name.html) | The name of another TextLineSpecification to inherit from. |
| [`ApplicableTextLineNumbers`](applicable-text-line-numbers.html) | The text line numbers this specification applies to. |

## Recognition Settings

| Parameter | Description |
|:----------|:------------|
| [`CharacterModelName`](character-model-name.html) | The name of the character recognition model. |
| [`TextLineRecModelName`](text-line-rec-model-name.html) | The name of the text line recognition model. |
| [`CharHeightRange`](char-height-range.html) | The expected character height range. |
| [`CharacterNormalizationModes`](character-normalization-modes.html) | The modes for character normalization. |
| [`StringLengthRange`](string-length-range.html) | The expected string length range. |
| [`StringRegexPattern`](string-regex-pattern.html) | The regex pattern for validating recognized strings. |
| [`ConfusableCharactersCorrection`](confusable-characters-correction.html) | The settings for confusable characters correction. |

## Processing Modes

| Parameter | Description |
|:----------|:------------|
| [`BinarizationModes`](binarization-modes.html) | The modes for binarization. |
| [`GrayscaleEnhancementModes`](grayscale-enhancement-modes.html) | The modes for grayscale enhancement. |

## Groups & Concatenation

| Parameter | Description |
|:----------|:------------|
| [`ExpectedGroupsCount`](expected-groups-count.html) | The expected number of text line groups. |
| [`SubGroups`](sub-groups.html) | The sub-group definitions. |
| [`ReferenceGroupName`](reference-group-name.html) | The name of the reference group. |
| [`TextLinesCount`](text-lines-count.html) | The expected number of text lines. |
| [`Position`](position.html) | The position of the text line. |

## Output & Concatenation

| Parameter | Description |
|:----------|:------------|
| [`OutputResults`](output-results.html) | Whether to output results for this specification. |
| [`ConcatResults`](concat-results.html) | Whether to concatenate results. |
| [`ConcatSeparator`](concat-separator.html) | The separator for concatenated results. |
| [`ConcatStringLengthRange`](concat-string-length-range.html) | The length range for concatenated strings. |
| [`ConcatStringRegexPattern`](concat-string-regex-pattern.html) | The regex pattern for concatenated strings. |
