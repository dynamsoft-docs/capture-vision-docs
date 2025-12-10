---
layout: default-layout
title: RecognizeRawTextLinesStage - Dynamsoft Label Recognizer Parameters
description: The RecognizeRawTextLinesStage recognizes the raw values of text lines.
keywords: Recognize Raw Text Lines Stage
---

# RecognizeRawTextLinesStage

`RecognizeRawTextLinesStage` recognizes the raw values of text lines. In JSON, it is represented as a Stage object with `"Stage": "SST_RECOGNIZE_RAW_TEXT_LINES"`.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_RECOGNIZE_RAW_TEXT_LINES")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-text-lines-recognition.html#stagearray) within [TextLinesRecognitionSection]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-text-lines-recognition.html)

**Example:**

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

> [!NOTE]
> - This snippet shows a Stage object configured for recognizing raw text lines.
> - To use it, add this object to the `StageArray` within a [TextLinesRecognitionSection]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-text-lines-recognition.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_RECOGNIZE_RAW_TEXT_LINES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_RECOGNIZE_RAW_TEXT_LINES"` |

### DictionaryPath

Sets the path of the dictionary file. See [`DictionaryPath`](dictionary-path.md) for details.

### DictionaryCorrectionThresholds

Sets the threshold of dictionary error correction. See [`DictionaryCorrectionThresholds`](dictionary-correction-thresholds.md) for details.

### ConfusableCharactersPath

Sets the path to the .data file containing characters features for confusable characters telling. See [`ConfusableCharactersPath`](confusable-characters-path.md) for details.

### ClusterSamplesCountThreshold

Sets the threshold of cluster samples count. See [`ClusterSamplesCountThreshold`](cluster-samples-count-threshold.md) for details.

### OverlappingCharactersPath

Sets the path to the .data file containing characters features for overlapping matching. See [`OverlappingCharactersPath`](overlapping-characters-path.md) for details.

### EnableRegexForceCorrection

Sets whether to enable forced correction based on the RegexPattern. See [`EnableRegexForceCorrection`](enable-regex-force-correction.md) for details.
