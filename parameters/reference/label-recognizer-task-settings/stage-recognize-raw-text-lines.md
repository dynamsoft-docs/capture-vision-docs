---
layout: default-layout
title: RecognizeRawTextLinesStage - Dynamsoft Label Recognizer Parameters
description: The parameter defines Recognize Raw Text Lines Stage under the Text Line Recognition Section.
keywords: Recognize Raw Text Lines Stage
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# RecognizeRawTextLinesStage Object

The `RecognizeRawTextLinesStage` is designed at the stage level to recognize the raw values of text-lines.

```json
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
    "ConfusableCharactersPath": "",
    "ClusterSamplesCountThreshold": 0,
    "OverlappingCharactersPath": "OverlappingChars.data", 
    "EnableRegexForceCorrection": 1
}
```

## Stage

The stage is named `SST_RECOGNIZE_RAW_TEXT_LINES`.

## DictionaryPath

Parameter [`DictionaryPath`](dictionary-path.md) sets the path of the dictionary file.

## DictionaryCorrectionThresholds

Parameter [`DictionaryCorrectionThresholds`](dictionary-correction-thresholds.md) sets the threshold of dictionary error correction.

## ConfusableCharactersPath

Parameter [`ConfusableCharactersPath`](confusable-characters-path.md) sets the path to the .data file containing characters features for confusable characters telling.

## ClusterSamplesCountThreshold

Parameter [`ClusterSamplesCountThreshold`](cluster-samples-count-threshold.md) sets the threshold of cluster samples count.

## OverlappingCharactersPath

Parameter [`OverlappingCharactersPath`](overlapping-characters-path.md) sets the path to the .data file containing characters features for overlapping matching.

## EnableRegexForceCorrection

Parameter [`EnableRegexForceCorrection`](enable-regex-force-correction.md) sets whether to enable forced correction based on the RegexPattern.
