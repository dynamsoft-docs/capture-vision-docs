---
layout: default-layout
title: PredetectRegionsStage - Dynamsoft Document Normalizer Parameters
description: The PredetectRegionsStage identifies regions of interest (ROIs).
keywords: Predetect Regions Stage
---

# PredetectRegionsStage

`PredetectRegionsStage` identifies regions of interest (ROIs). The pre-detected region may be identified based on color features, grayscale features, or neural network localization. In JSON, it is represented as a Stage object with `"Stage": "SST_PREDETECT_REGIONS"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_PREDETECT_REGIONS")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-regions-predetection.html#stagearray) within [RegionsPredetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-regions-predetection.html)

**Example:**

```json
{
    "Stage": "SST_PREDETECT_REGIONS",
    "RegionPredetectionModes": [
        {
            "Mode": "RPM_GENERAL"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for region predetection.
> - To use it, add this object to the `StageArray` within a [RegionsPredetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-regions-predetection.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_PREDETECT_REGIONS`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_PREDETECT_REGIONS"` |

### RegionPredetectionModes

Controls how to find a region of interest (ROI) within the image or frame. See [`RegionPredetectionModes`]({{ site.dcvb_parameters_reference }}image-parameter/region-predetection-modes.html) for details. 
