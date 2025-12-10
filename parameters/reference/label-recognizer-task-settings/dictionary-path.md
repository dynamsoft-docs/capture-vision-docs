---
layout: default-layout
title: DictionaryPath - Dynamsoft Label Recognizer Parameters
description: The parameter DictionaryPath of Dynamsoft Label Recognizer defines the path of the dictionary file
keywords: user dictionary, text correction
---

# DictionaryPath

Parameter `DictionaryPath` sets the path of the dictionary file.

## JSON Structure

**Location in template:**

```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_RECOGNIZE_RAW_TEXT_LINES")
            └── DictionaryPath
```

**Parent object:** [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html)

**Example:**

```json
{
    "DictionaryPath": "D:\\DictModel\\nutrition.txt"
}
```

> [!NOTE]
> - This snippet shows only the `DictionaryPath` parameter.
> - To use it, embed this parameter within a [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json)

## Parameter Details

| DictionaryPath Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The absolute file path.|
| **Default Value**<br>"" |
| **Remarks**<br>" " indicates that the dictionary is not enabled. It works together with the [DictionaryCorrectionThresholds](dictionary-correction-thresholds.md) parameter to perform error correction during the recognition process.|
