---
layout: default-layout
title: RemoveTextZonesFromBinaryStage - Dynamsoft Capture Vision Parameters
description: The RemoveTextZonesFromBinaryStage removes text zones from the binary image.
keywords: Remove Text Zones from Binary Stage
---

# RemoveTextZonesFromBinaryStage

`RemoveTextZonesFromBinaryStage` removes text zones from the binary image. In JSON, it is represented as a Stage object with `"Stage": "SST_REMOVE_TEXT_ZONES_FROM_BINARY"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_REMOVE_TEXT_ZONES_FROM_BINARY")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_REMOVE_TEXT_ZONES_FROM_BINARY",
    "IfEraseTextZone": 1
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for removing text zones from binary images.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_REMOVE_TEXT_ZONES_FROM_BINARY`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_REMOVE_TEXT_ZONES_FROM_BINARY"` |

### IfEraseTextZone

Defines whether to erase text zones from the binary image. See [`IfEraseTextZone`](if-erase-text-zone.md) for details.
