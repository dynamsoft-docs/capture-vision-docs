---
layout: default-layout
title: InputColorImageStage - Dynamsoft Capture Vision Parameters
description: The InputColorImageStage represents the starting stage of each section, serving as a placeholder for the input color image.
keywords: Input Color Image Stage
---

# InputColorImageStage

`InputColorImageStage` represents the starting stage of each section in the image processing pipeline. It acts as a placeholder marking the entry point where the original color image is first received for processing within a section. In JSON, it is represented as a Stage object with `"Stage": "SST_INPUT_COLOR_IMAGE"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_INPUT_COLOR_IMAGE")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_INPUT_COLOR_IMAGE"
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for the input color image.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_INPUT_COLOR_IMAGE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_INPUT_COLOR_IMAGE"` |
