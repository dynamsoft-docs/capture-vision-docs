---
layout: default-layout
title:  TextLineSpecification Object Introduction
description: Introduced the define of TextLineSpecification objects for Dynamsoft Capture Vision.
keywords: Text line specification
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextLineSpecification Object

A `TextLineSpecification` object is used to specify a certain line of text line in the `TargetROI` and configure its processing parameters. `TextLineSpecification` is an auxiliary setting that supports the `LabelRecognizerTaskSettings`

```json
{
    "Name":"LS_1",
    "CharacterModelName" : "NumberLetter",
    "GrayscaleEnhancementModes" : [],
    "BinarizationModes" : [],
    "CharacterNormalizationModes" : [],
    "BaseTextLineSpecificationName" : "LS_0",
    "ApplicableTextLineNumbers":"",
    "StringLengthRange" : [44,44],
    "StringRegExPattern" : "",
    "FirstPoint" : [ 0, 0 ],
    "SecondPoint" : [ 100, 0 ],
    "ThirdPoint" : [ 100, 20 ],
    "FourthPoint" : [ 0, 20 ],
    "CharHeightRange" : [ 800, 1000, 1 ]
}
```

<div align="center">
   <p><img src="../assets/text-line-specification.png" alt="text-line-specification" width="30%" /></p>
   <p></p>
</div>

## Why Use this Parameter
<!--Draft-->
- There exists a text line that diferent from the others. Set special model or parameters for a certain text line.
- Each text line have different styles.
- There exists some recognizable charaters in the lines but they are not the targeting content.

## Definition

### Select the Character Model

The default model is "NumberLetter" which recognize all general number and letter characters.

### Configure ImageProcessing Modes

`GrayscaleEnhancementModes`, `BinarizationModes` and `CharacterNormalizationModes`

### Specify the Target Text Lines

- Where the text lines are located in the TargetROI.
- Which text line use the settings.

### Others

Use `BaseTextLineSpecificationName` to make minor changes on a existing `TextLineSpecification` object.

## As a LabelRecognizerTaskSetting Parameter

`TextLineSpecificationNameArray` is a parameter of the `LabelRecognizerTaskSetting` object.

- Without TextLineSpecificationNameArray:
- Not all the text lines are covered by `TextLineSpecificationNameArray`:
- All the text lines are covered by `TextLineSpecificationNameArray`:
