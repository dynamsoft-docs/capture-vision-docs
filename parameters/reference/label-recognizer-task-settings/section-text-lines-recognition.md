---
layout: default-layout
title: TextLineRecognitionSection - Dynamsoft Label Recognizer Parameters
description: The TextLineRecognitionSection recognizes text from localized text-line regions.
keywords: TextLineRecognitionSection
---

# TextLineRecognitionSection

`TextLineRecognitionSection` recognizes text from localized text-line regions. In JSON, it is represented as a Section object with `"Section": "ST_TEXT_LINE_RECOGNITION"`.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object where Section = "ST_TEXT_LINE_RECOGNITION")
```

**Parent object:** [SectionArray]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-array.html)

**Example:**

```json
{
    "Section": "ST_TEXT_LINE_RECOGNITION",
    "ImageParameterName": "ip_dlrDefault",
    "StageArray": [
        {
            "Stage": "SST_RECOGNIZE_RAW_TEXT_LINES"
        },
        {
            "Stage": "SST_ASSEMBLE_TEXT_LINES"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Section object configured for text line recognition.
> - To use it, add this object to the [SectionArray]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/section-array.html) of a [LabelRecognizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/label-recognizer-task-settings.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Section

Specifies the section type. Fixed value: `ST_TEXT_LINE_RECOGNITION`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"ST_TEXT_LINE_RECOGNITION"` |

### ImageParameterName

Specifies the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object to apply in the stages of this section.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>Must be the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object defined under `ImageParameterOptions` |
| **Default Value**<br>`""` |

### StageArray

Specifies the stage objects within this section. The `TextLineRecognitionSection` consists of the following stages:

| Stage | Description |
|-------|-------------|
| [RecognizeRawTextLinesStage](stage-recognize-raw-text-lines.md) (`SST_RECOGNIZE_RAW_TEXT_LINES`) | Recognizes the raw values of text-lines. |
| [AssembleTextLinesStage](stage-assemble-text-lines.md) (`SST_ASSEMBLE_TEXT_LINES`) | Assembles grouped text-lines into a single text-line. |
