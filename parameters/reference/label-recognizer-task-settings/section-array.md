---
layout: default-layout
title: SectionArray - Dynamsoft Label Recognizer Parameters
description: The parameter SectionArray defines which sections exist under the LabelRecognizerTask.
keywords: Section Array parameter
---

# SectionArray

Parameter `SectionArray` defines which sections exist under the `LabelRecognizerTask`. A `Section` is a sequence of `Stages` that form a relatively complete processing unit, producing milestone results that include location information along with other details.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray
```

**Parent object:** [LabelRecognizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/label-recognizer-task-settings.html) object

**Example:**

```json
{
    "SectionArray": [
        {
            "Section": "ST_REGION_PREDETECTION"
        },
        {
            "Section": "ST_TEXT_LINE_LOCALIZATION"
        },
        {
            "Section": "ST_TEXT_LINE_RECOGNITION"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `SectionArray` parameter.
> - To use it, embed this parameter within a [LabelRecognizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/label-recognizer-task-settings.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The `LabelRecognizerTask` includes the following sections:

* [RegionPredetectionSection](section-regions-predetection.md) (`ST_REGION_PREDETECTION`)
  * Designed to find regions of interest (ROIs) and thus ignore other parts of the image during subsequent processing.
* [TextLineLocalizationSection](section-text-lines-localization.md) (`ST_TEXT_LINE_LOCALIZATION`)
  * Designed to detect the exact locations of text-lines.
* [TextLineRecognitionSection](section-text-lines-recognition.md) (`ST_TEXT_LINE_RECOGNITION`)
  * Designed to recognize the text from the text-line areas identified in the previous `TextLineLocalizationSection` section.
