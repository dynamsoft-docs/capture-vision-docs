---
layout: default-layout
title: FindContoursStage - Dynamsoft Capture Vision Parameters
description: The FindContoursStage finds contours in the image.
keywords: Find Contours Stage
---

# FindContoursStage

`FindContoursStage` finds contours in the image. In JSON, it is represented as a Stage object with `"Stage": "SST_FIND_CONTOURS"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_FIND_CONTOURS")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_FIND_CONTOURS"
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for finding contours.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_FIND_CONTOURS`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_FIND_CONTOURS"` |
