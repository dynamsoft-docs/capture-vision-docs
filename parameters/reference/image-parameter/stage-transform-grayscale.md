---
layout: default-layout
title: TransformGrayscaleStage - Dynamsoft Capture Vision Parameters
description: The TransformGrayscaleStage transforms the grayscale image.
keywords: Transform Grayscale Stage
---

# TransformGrayscaleStage

`TransformGrayscaleStage` transforms the grayscale image. In JSON, it is represented as a Stage object with `"Stage": "SST_TRANSFORM_GRAYSCALE"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_TRANSFORM_GRAYSCALE")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_TRANSFORM_GRAYSCALE",
    "GrayscaleTransformationModes": [
        {
            "Mode": "GTM_ORIGINAL"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for transforming grayscale images.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_TRANSFORM_GRAYSCALE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_TRANSFORM_GRAYSCALE"` |

### GrayscaleTransformationModes

Defines how to transform the grayscale image. See [`GrayscaleTransformationModes`](grayscale-transformation-modes.md) for details.
