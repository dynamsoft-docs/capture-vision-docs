---
layout: default-layout
title: Index - Dynamsoft Label Recognizer TextLineSpecification Parameters
description: The index of TextLineSpecification parameters.
keywords: TextLineSpecification, parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/text-line-specification/index.html
---

# TextLineSpecification Parameters

| Parameter Name  | Description |
| ----------------------------------- | ----------- |
| [`ApplicableTextLineNumbers`](applicable-text-line-numbers.md) | Defines the line numers of the targeting lines which are specified by the `TextLineSpecification` object. |
| [`BaseTextLineSpecificationName`](base-text-line-specification-name.md) | Defines the name of another `BaseTextLineSpecificationName` object. |
| [`CharHeightRange`](char-height-range.md) | Defines the range of the character height. |
| [`CharacterModelName`](character-model-name.md) | Defines the name of the character model. |
| [`CharacterNormalizationModes`](character-normalization-modes.md) | Defines an array of character normalization mode to implement. |
| [`FirstPoint`](position.md#firstpoint) | The top-left vertex coordinate of the the text line. |
| [`SecondPoint`](position.md#secondpoint) | The top-right vertex coordinate of the the text line. |
| [`ThirdPoint`](position.md#thirdpoint) | The bottom-right vertex coordinate of the the text line. |
| [`FourthPoint`](position.md#fourthpoint) | The bottom-left vertex coordinate of the the text line. |
| [`Name`](name.md) | Defines the name of a `TextLineSpecification` object, which serves as its unique identifier. |
| [`BinarizationModes`](binarization-modes.md) | Helps control the process of binarization, i.e., converting a grayscale image to a binary image. |
| [`GrayscaleEnhancementModes`](grayscale-enhancement-modes.md) | Provides some image processing methods to enhance the grayscale quality of the text line area. |
| [`StringLengthRange`](string-length-range.md) | Sets the range of string length for each recognized line. |
| [`StringRegExPattern`](string-regex-pattern.md) | Specifies the regular expression pattern of the string within a line. It is used to correct the recognized line text. |
| [`ConcatStringLengthRange`](concat-string-length-range.md) | Sets the range of string length for the concated recognized text lines. |
| [`ConcatStringRegExPattern`](concat-string-regex-pattern.md) | Specifies the regular expression pattern of the concated text lines. It is used to correct the recognized line text. |
| [`ConcatSeparator`](concat-separator.md) | Defines the concat separator used to join multiple lines of text. |
| [`ConcatResults`](concat-results.md) | Defines whether to concatenate multiple lines of text.  |
| [`OutputResults`](output-results.md) | Defines whether to enable the output of the `TextLineSpecification` object. |
| [`SubGroups`](sub-groups.md) | Defines the layout of subgroups of the `TextLineSpecification` object. |
| [`ReferenceGroupName`](reference-group-name.md) | Defines the reference group for space layout configuration. |
| [`TextLinesCount`](text-lines-count.md) | Defines the expected number of text lines for the `TextLineSpecification` object. |
