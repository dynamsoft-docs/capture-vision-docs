---
layout: default-layout
title: StringLengthRange - Dynamsoft Label Recognizer Parameters
description: The parameter StringLengthRange of Dynamsoft Label Recognizer defines the range of string lengths for concatenated strings of recognized text lines.
keywords: text lines, concatenated strings length
---

# StringLengthRange

Parameter `StringLengthRange` sets the range of string lengths for concatenated strings of recognized text lines.

## JSON Structure

**Location in template:**

```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_ASSEMBLE_TEXT_LINES")
            └── StringLengthRange
```

**Parent object:** [AssembleTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-assemble-text-lines.html)

**Example:**

```json
{
    "StringLengthRange": [3,200]
}
```

> [!NOTE]
> - This snippet shows only the `StringLengthRange` parameter.
> - To use it, embed this parameter within a [AssembleTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-assemble-text-lines.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json)

## Parameter Details

| StringLengthRange Parameter Details |
| :----------------------------------- |
| **Type**<br>*int[]* |
| **Range**<br>The array contains only two elements, corresponding to the lower and upper bounds of the Range, respectively. The value range is [0, 0x7fffffff].|
| **Default Value**<br>[3,200] |
| **Remarks**<br>The first element is the lower bound and the second is the upper bound.|
