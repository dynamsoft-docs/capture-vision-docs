---
layout: default-layout
title: ScaleImageStage - Dynamsoft Capture Vision Parameters
description: The ScaleImageStage down/up scales the image.
keywords: Scale Image Stage
---

# ScaleImageStage

`ScaleImageStage` down/up scales the image. In JSON, it is represented as a Stage object with `"Stage": "SST_SCALE_IMAGE"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_SCALE_IMAGE")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_SCALE_IMAGE",
    "ImageScaleSetting": {
        "ScaleType": "ST_SCALE_DOWN",
        "ReferenceEdge": "RE_SHORTER_EDGE",
        "EdgeLengthThreshold": 2300
    }
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for scaling images.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_SCALE_IMAGE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_SCALE_IMAGE"` |

### ImageScaleSetting

Defines how to scale the image. See [`ImageScaleSetting`](image-scale-settings.md) for details.
