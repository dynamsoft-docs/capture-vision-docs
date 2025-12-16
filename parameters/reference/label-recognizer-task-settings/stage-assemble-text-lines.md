---
layout: default-layout
title: AssembleTextLinesStage - Dynamsoft Label Recognizer Parameters
description: The AssembleTextLinesStage assembles the grouped text lines into a single text line.
keywords: Assemble Text Lines Stage
---

# AssembleTextLinesStage

`AssembleTextLinesStage` assembles the grouped text lines into a single text line. In JSON, it is represented as a Stage object with `"Stage": "SST_ASSEMBLE_TEXT_LINES"`.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_ASSEMBLE_TEXT_LINES")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-text-lines-recognition.html#stagearray) within [TextLinesRecognitionSection]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-text-lines-recognition.html)

**Example:**

```json
{
    "Stage": "SST_ASSEMBLE_TEXT_LINES",
    "StringLengthRange": [3, 200],
    "StringRegExPattern": ""
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for assembling text lines.
> - To use it, add this object to the `StageArray` within a [TextLinesRecognitionSection]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-text-lines-recognition.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_ASSEMBLE_TEXT_LINES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_ASSEMBLE_TEXT_LINES"` |

### StringLengthRange

Sets the range of string lengths for concatenated strings of recognized text lines. See [`StringLengthRange`](string-length-range.md) for details.

### StringRegExPattern

Specifies the regular expression pattern for concatenated strings of recognized text lines. See [`StringRegExPattern`](string-regex-pattern.md) for details.
