---
layout: default-layout
title: LocalizeTextLinesStage - Dynamsoft Label Recognizer Parameters
description: The LocalizeTextLinesStage detects the exact locations of text lines.
keywords: Localize Text Lines Stage
---

# LocalizeTextLinesStage

`LocalizeTextLinesStage` detects the exact locations of text lines. In JSON, it is represented as a Stage object with `"Stage": "SST_LOCALIZE_TEXT_LINES"`.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_LOCALIZE_TEXT_LINES")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-text-lines-localization.html#stagearray) within [TextLinesLocalizationSection]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-text-lines-localization.html)

**Example:**

```json
{
    "Stage": "SST_LOCALIZE_TEXT_LINES"
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for localizing text lines.
> - To use it, add this object to the `StageArray` within a [TextLinesLocalizationSection]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-text-lines-localization.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_LOCALIZE_TEXT_LINES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_LOCALIZE_TEXT_LINES"` |
