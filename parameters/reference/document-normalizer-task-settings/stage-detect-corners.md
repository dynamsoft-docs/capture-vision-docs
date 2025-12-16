---
layout: default-layout
title: DetectCornersStage - Dynamsoft Document Normalizer Parameters
description: The DetectCornersStage detects corners of quadrilaterals that meet the specified conditions.
keywords: Detect Corners Stage
---

# DetectCornersStage

`DetectCornersStage` detects corners of quadrilaterals that meet the specified conditions. In JSON, it is represented as a Stage object with `"Stage": "SST_DETECT_CORNERS"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_DETECT_CORNERS")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html#stagearray) within [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html)

**Example:**

```json
{
    "Stage": "SST_DETECT_CORNERS",
    "CornerAngleRange": {
        "MaxValue": 110,
        "MinValue": 70
    }
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for detecting corners.
> - To use it, add this object to the `StageArray` within a [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_DETECT_CORNERS`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_DETECT_CORNERS"` |

### CornerAngleRange

Specifies the range of angles (in degrees) of the extracted corners. See [`CornerAngleRange`](corner-angle-range.md) for details.