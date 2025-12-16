---
layout: default-layout
title: BinarizeImageStage - Dynamsoft Capture Vision Parameters
description: The BinarizeImageStage transfers a grayscale image into a binary image.
keywords: Binarize Image Stage
---

# BinarizeImageStage

`BinarizeImageStage` transfers a grayscale image into a binary image. In JSON, it is represented as a Stage object with `"Stage": "SST_BINARIZE_IMAGE"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_BINARIZE_IMAGE")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_BINARIZE_IMAGE",
    "BinarizationModes": [
        {
            "Mode": "BM_LOCAL_BLOCK"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for binarizing images.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_BINARIZE_IMAGE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_BINARIZE_IMAGE"` |

### BinarizationModes

Defines the binarization options. See [`BinarizationModes`](binarization-modes.md) for details.
