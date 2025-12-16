---
layout: default-layout
title: StringRegExPattern - Dynamsoft Label Recognizer Parameters
description: The parameter StringRegExPattern of Dynamsoft Label Recognizer defines the regular expression pattern for concatenated strings of recognized text lines.
keywords: text lines, concatenated strings, regular expression
---

# StringRegExPattern

Parameter `StringRegExPattern` specifies the regular expression pattern for concatenated strings of recognized text lines.

## JSON Structure

**Location in template:**

```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_ASSEMBLE_TEXT_LINES")
            └── StringRegExPattern
```

**Parent object:** [AssembleTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-assemble-text-lines.html)

**Example:**

```json
{
    "StringRegExPattern": ""
}
```

> [!NOTE]
> - This snippet shows only the `StringRegExPattern` parameter.
> - To use it, embed this parameter within a [AssembleTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-assemble-text-lines.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json)

## Parameter Details

| StringRegExPattern Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>All standard regular expressions.|
| **Default Value**<br>"" |
| **Remarks**<br>This is a filtering parameter. After all recognized text lines are concatenated, they will be matched against this regular expression. Results that do not match will not be output. |
