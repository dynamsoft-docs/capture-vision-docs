---
layout: default-layout
title: EnhanceImageStage - Dynamsoft Document Normalizer Parameters
description: The EnhanceImageStage adjusts the image quality.
keywords: Enhance Image Stage
---

# EnhanceImageStage

`EnhanceImageStage` adjusts the image quality, such as changing the brightness, contrast, and the color mode of the image. In JSON, it is represented as a Stage object with `"Stage": "SST_ENHANCE_IMAGE"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_ENHANCE_IMAGE")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-image-enhancement.html#stagearray) within [ImageEnhancementSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-image-enhancement.html)

**Example:**

```json
{
    "Stage": "SST_ENHANCE_IMAGE",
    "ColourMode": "ICM_COLOUR",
    "Brightness": 0,
    "Contrast": 0
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for enhancing images.
> - To use it, add this object to the `StageArray` within an [ImageEnhancementSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-image-enhancement.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_ENHANCE_IMAGE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_ENHANCE_IMAGE"` |

### ColourMode

Defines the output colour mode of the target image. See [`ColourMode`](colour-mode.md) for details.

### Brightness

Defines the brightness of the target image. See [`Brightness`](brightness.md) for details.

### Contrast

Specifies the contrast of the target image. See [`Contrast`](contrast.md) for details.