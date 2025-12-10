---
layout: default-layout
title: OverlappingCharactersPath - Dynamsoft Label Recognizer Parameters
description: The parameter OverlappingCharactersPath of Dynamsoft Label Recognizer defines the path to the .data file containing characters features for overlapping matching.
keywords: characters overlapping matching
---

# OverlappingCharactersPath

The parameter `OverlappingCharactersPath` sets the path to the .data file containing characters features for overlapping matching.

## JSON Structure

**Location in template:**

```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_RECOGNIZE_RAW_TEXT_LINES")
            └── OverlappingCharactersPath
```

**Parent object:** [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html)

**Example:**

```json
{
    "OverlappingCharactersPath": "D:\\YourApp\\OverlappingChars.data"
}
```

> [!NOTE]
> - This snippet shows only the `OverlappingCharactersPath` parameter.
> - To use it, embed this parameter within a [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json)

## Parameter Details

| OverlappingCharactersPath Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The absolute file path or the path relative to the Dynamsoft Label Recognizer library.|
| **Default Value**<br>"" |
| **Remarks**<br>"" indicates that the characters overlapping matching is not enabled. |
