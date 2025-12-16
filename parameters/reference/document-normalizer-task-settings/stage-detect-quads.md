---
layout: default-layout
title: DetectQuadsStage - Dynamsoft Document Normalizer Parameters
description: The DetectQuadsStage detects complete quadrilaterals.
keywords: Detect Quads Stage
---

# DetectQuadsStage

`DetectQuadsStage` detects complete quadrilaterals. In JSON, it is represented as a Stage object with `"Stage": "SST_DETECT_QUADS"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_DETECT_QUADS")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html#stagearray) within [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html)

**Example:**

```json
{
    "Stage": "SST_DETECT_QUADS",
    "QuadrilateralDetectionModes": [
        {
            "Mode": "QDM_GENERAL"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for detecting quads.
> - To use it, add this object to the `StageArray` within a [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_DETECT_QUADS`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_DETECT_QUADS"` |

### QuadrilateralDetectionModes

Controls the quadrilateral detection process on an image. See [`QuadrilateralDetectionModes`](quadrilateral-detection-modes.md) for details.