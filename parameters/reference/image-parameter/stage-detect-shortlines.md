---
layout: default-layout
title: DetectShortLinesStage - Dynamsoft Capture Vision Parameters
description: The DetectShortLinesStage detects short lines for document boundary detection.
keywords: Detect Short Lines Stage
---

# DetectShortLinesStage

`DetectShortLinesStage` detects short lines for document boundary detection. In JSON, it is represented as a Stage object with `"Stage": "SST_DETECT_SHORTLINES"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_DETECT_SHORTLINES")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_DETECT_SHORTLINES",
    "ShortlineDetectionMode": {
        "Mode": "SDM_GENERAL",
        "Sensitivity": 3
    }
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for detecting short lines.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_DETECT_SHORTLINES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_DETECT_SHORTLINES"` |

### ShortlineDetectionMode

Defines how to detect short lines. See [`ShortlineDetectionMode`](shortline-detection-mode.md) for details.
