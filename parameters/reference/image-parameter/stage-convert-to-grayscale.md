---
layout: default-layout
title: ConvertToGrayscaleStage - Dynamsoft Capture Vision Parameters
description: The ConvertToGrayscaleStage converts a colour image to a grayscale image.
keywords: Convert to Grayscale Stage
---

# ConvertToGrayscaleStage

`ConvertToGrayscaleStage` converts a colour image to a grayscale image. In JSON, it is represented as a Stage object with `"Stage": "SST_CONVERT_TO_GRAYSCALE"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_CONVERT_TO_GRAYSCALE")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_CONVERT_TO_GRAYSCALE",
    "ColourConversionModes": [
        {
            "Mode": "CICM_GENERAL"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for converting to grayscale.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_CONVERT_TO_GRAYSCALE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_CONVERT_TO_GRAYSCALE"` |

### ColourConversionModes

Defines how to convert a colour image to a grayscale image. See [`ColourConversionModes`](colour-conversion-modes.md) for details.
