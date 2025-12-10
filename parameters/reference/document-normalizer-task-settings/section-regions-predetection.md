---
layout: default-layout
title: RegionPredetectionSection - Dynamsoft Document Normalizer Parameters
description: The RegionPredetectionSection identifies regions of interest (ROIs) for subsequent processing.
keywords: RegionPredetectionSection
---

# RegionPredetectionSection

`RegionPredetectionSection` identifies regions of interest (ROIs), allowing subsequent processing to ignore other parts of the image. In JSON, it is represented as a Section object with `"Section": "ST_REGION_PREDETECTION"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object where Section = "ST_REGION_PREDETECTION")
```

**Parent object:** [SectionArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-array.html)

**Example:**

```json
{
    "Section": "ST_REGION_PREDETECTION",
    "ImageParameterName": "ip_ddnDefault",
    "StageArray": [
        {
            "Stage": "SST_PREDETECT_REGIONS"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Section object configured for region predetection.
> - To use it, add this object to the [SectionArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-array.html) of a [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Section

Specifies the section type. Fixed value: `ST_REGION_PREDETECTION`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"ST_REGION_PREDETECTION"` |

### ImageParameterName

Specifies the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object to apply in the stages of this section.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>Must be the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object defined under `ImageParameterOptions` |
| **Default Value**<br>`""` |

### StageArray

Specifies the stage objects within this section. The `RegionPredetectionSection` consists of the following stages:

| Stage | Description |
|-------|-------------|
| [PredetectRegionsStage](./stage-predetect-regions.md) (`SST_PREDETECT_REGIONS`) | Identifies regions of interest (ROIs). |
