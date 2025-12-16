---
layout: default-layout
title: DetectTextZonesStage - Dynamsoft Capture Vision Parameters
description: The DetectTextZonesStage detects text zones on the image.
keywords: Detect Text Zones Stage
---

# DetectTextZonesStage

`DetectTextZonesStage` detects text zones on the image. In JSON, it is represented as a Stage object with `"Stage": "SST_DETECT_TEXT_ZONES"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_DETECT_TEXT_ZONES")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_DETECT_TEXT_ZONES",
    "TextDetectionMode": {
        "Mode": "TTDM_LINE"
    }
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for detecting text zones.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_DETECT_TEXT_ZONES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_DETECT_TEXT_ZONES"` |

### TextDetectionMode

Defines how to detect text zones. See [`TextDetectionMode`](text-detection-mode.md) for details.
