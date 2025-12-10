---
layout: default-layout
title: ConfusableCharactersPath - Dynamsoft Label Recognizer Parameters
description: The parameter ConfusableCharactersPath of Dynamsoft Label Recognizer defines the path to the .data file containing standard characters features for confusable characters telling.
keywords: confusable characters path
---

# ConfusableCharactersPath

The parameter `ConfusableCharactersPath` sets the path to the .data file containing characters features for confusable characters telling.

## JSON Structure

**Location in template:**

```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_RECOGNIZE_RAW_TEXT_LINES")
            └── ConfusableCharactersPath
```

**Parent object:** [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html)

**Example:**

```json
{
    "ConfusableCharactersPath": "D:\\YourApp\\ConfusableChars.data"
}
```

> [!NOTE]
> - This snippet shows only the `ConfusableCharactersPath` parameter.
> - To use it, embed this parameter within a [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json)

## Parameter Details

| ConfusableCharactersPath Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The absolute file path or the path relative to the Dynamsoft Label Recognizer library.|
| **Default Value**<br>"" |
| **Remarks**<br>"" indicates that the confusable characters telling is not enabled. It works together with the [ConfusableCharactersCorrection](../text-line-specification/confusable-characters-correction.md) parameter to perform confusable characters correction during the recognition process.|
