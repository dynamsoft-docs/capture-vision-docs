---
layout: default-layout
title: DetectTextureStage - Dynamsoft Capture Vision Parameters
description: The DetectTextureStage detects texture on the image.
keywords: Detect Texture Stage
---

# DetectTextureStage

`DetectTextureStage` detects texture on the image. In JSON, it is represented as a Stage object with `"Stage": "SST_DETECT_TEXTURE"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_DETECT_TEXTURE")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_DETECT_TEXTURE",
    "TextureDetectionModes": [
        {
            "Mode": "TDM_GENERAL_WIDTH_CONCENTRATION"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for detecting texture.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_DETECT_TEXTURE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_DETECT_TEXTURE"` |

### TextureDetectionModes

Defines how to detect texture. See [`TextureDetectionModes`](texture-detection-modes.md) for details.
