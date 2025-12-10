---
layout: default-layout
title: ImageEnhancementSection - Dynamsoft Document Normalizer Parameters
description: The ImageEnhancementSection adjusts the image quality.
keywords: ImageEnhancementSection
---

# ImageEnhancementSection

`ImageEnhancementSection` adjusts the image quality. In JSON, it is represented as a Section object with `"Section": "ST_IMAGE_ENHANCEMENT"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object where Section = "ST_IMAGE_ENHANCEMENT")
```

**Parent object:** [SectionArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-array.html)

**Example:**

```json
{
    "Section": "ST_IMAGE_ENHANCEMENT",
    "ImageParameterName": "ip_ddnDefault",
    "StageArray": [
        {
            "Stage": "SST_ENHANCE_IMAGE"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Section object configured for image enhancement.
> - To use it, add this object to the [SectionArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-array.html) of a [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Section

Specifies the section type. Fixed value: `ST_IMAGE_ENHANCEMENT`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"ST_IMAGE_ENHANCEMENT"` |

### ImageParameterName

Specifies the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object to apply in the stages of this section.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>Must be the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object defined under `ImageParameterOptions` |
| **Default Value**<br>`""` |

### StageArray

Specifies the stage objects within this section. The `ImageEnhancementSection` consists of the following stages:

| Stage | Description |
|-------|-------------|
| [EnhanceImageStage](./stage-enhance-image.md) (`SST_ENHANCE_IMAGE`) | Adjusts the image quality, such as changing the brightness, contrast, and color mode. |
