---
layout: default-layout
title: EnhanceGrayscaleStage - Dynamsoft Capture Vision Parameters
description: The EnhanceGrayscaleStage improves the quality of the grayscale image.
keywords: Enhance Grayscale Stage
---

# EnhanceGrayscaleStage

`EnhanceGrayscaleStage` improves the quality of the grayscale image. In JSON, it is represented as a Stage object with `"Stage": "SST_ENHANCE_GRAYSCALE"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_ENHANCE_GRAYSCALE")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_ENHANCE_GRAYSCALE",
    "GrayscaleEnhancementModes": [
        {
            "Mode": "GEM_GENERAL"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for enhancing grayscale images.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_ENHANCE_GRAYSCALE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_ENHANCE_GRAYSCALE"` |

### GrayscaleEnhancementModes

Defines how to enhance the grayscale image. See [`GrayscaleEnhancementModes`](grayscale-enhancement-modes.md) for details.
