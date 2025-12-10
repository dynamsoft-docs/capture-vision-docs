---
layout: default-layout
title: ImageScaleSetting - Dynamsoft Capture Vision Parameters
description: The parameter ImageScaleSetting of Dynamsoft Capture Vision is for controlling how to up or down scale the image.
keywords: scale-up, scale down, parameter reference, parameter
---

# ImageScaleSetting

Parameter `ImageScaleSetting` is for controlling how to up or down scale the image.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_SCALE_IMAGE")
        └── ImageScaleSetting
```

**Parent object:** [ScaleImageStage](stage-scale-image.md)

**Example:**

```json
{
    "ImageScaleSetting": {
        "ScaleType": "ST_SCALE_DOWN",
        "ReferenceEdge": "RE_SHORTER_EDGE",
        "EdgeLengthThreshold": 2300
    }
}
```

> [!NOTE]
> - This snippet shows only the `ImageScaleSetting` parameter.
> - To use it, embed this parameter within a [ScaleImageStage](stage-scale-image.md) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The `ImageScaleSetting` object includes the following parameters:

### ScaleType

Specifies whether to scale up or down the image.

| ScaleType Parameter Details |
| :-------------------------- |
| **Type**<br>*String* |
| **Value Range**<br>"ST_SCALE_DOWN", "ST_SCALE_UP" |
| **Default Value**<br>"ST_SCALE_DOWN" |

### ReferenceEdge

Specifies which edge (longer edge or shorter edge) to use when scaling the image.

| ReferenceEdge Parameter Details |
| :------------------------------ |
| **Type**<br>*String* |
| **Value Range**<br>"RE_SHORTER_EDGE", "RE_LONGER_EDGE" |
| **Default Value**<br>"RE_SHORTER_EDGE" |

### EdgeLengthThreshold

Specifies the threshold for scaling the image.

- If the `ScaleType` is set to "ST_SCALE_DOWN", the image will be continuously scaled down until the `ReferenceEdge` is shorter than the `EdgeLengthThreshold`.
- If the `ScaleType` is set to "ST_SCALE_UP", the image will be continuously scaled up until the `ReferenceEdge` is longer than the `EdgeLengthThreshold`.

| EdgeLengthThreshold Parameter Details |
| :----------------------------------- |
| **Type**<br>*int* |
| **Value Range**<br>[512, 0x7fffffff] |
| **Default Value**<br>2300 |
