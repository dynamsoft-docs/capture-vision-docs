---
layout: default-layout
title: TextLineLocalizationSection - Dynamsoft Label Recognizer Parameters
description: The TextLineLocalizationSection detects the exact locations of text-lines.
keywords: TextLineLocalizationSection
---

# TextLineLocalizationSection

`TextLineLocalizationSection` detects the exact locations of text-lines. In JSON, it is represented as a Section object with `"Section": "ST_TEXT_LINE_LOCALIZATION"`.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object where Section = "ST_TEXT_LINE_LOCALIZATION")
```

**Parent object:** [SectionArray]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-array.html)

**Example:**

```json
{
    "Section": "ST_TEXT_LINE_LOCALIZATION",
    "ImageParameterName": "ip_dlrDefault",
    "StageArray": [
        {
            "Stage": "SST_LOCALIZE_TEXT_LINES"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Section object configured for text line localization.
> - To use it, add this object to the [SectionArray]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-array.html) of a [LabelRecognizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/label-recognizer-task-settings.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Section

Specifies the section type. Fixed value: `ST_TEXT_LINE_LOCALIZATION`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"ST_TEXT_LINE_LOCALIZATION"` |

### ImageParameterName

Specifies the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object to apply in the stages of this section.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>Must be the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object defined under `ImageParameterOptions` |
| **Default Value**<br>`""` |

### StageArray

Specifies the stage objects within this section. The `TextLineLocalizationSection` consists of the following stages:

| Stage | Description |
|-------|-------------|
| [LocalizeTextLinesStage](stage-localize-text-lines.md) (`SST_LOCALIZE_TEXT_LINES`) | Detects the exact locations of text-lines. |
