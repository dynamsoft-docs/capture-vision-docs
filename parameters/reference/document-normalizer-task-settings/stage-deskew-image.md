---
layout: default-layout
title: DeskewImageStage - Dynamsoft Document Normalizer Parameters
description: The DeskewImageStage de-skews the quadrilateral to transform it into a rectangle.
keywords: Deskew Image Stage
---

# DeskewImageStage

`DeskewImageStage` de-skews the quadrilateral to transform it into a rectangle. In JSON, it is represented as a Stage object with `"Stage": "SST_DESKEW_IMAGE"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_DESKEW_IMAGE")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-deskewing.html#stagearray) within [DocumentDeskewingSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-deskewing.html)

**Example:**

```json
{
    "Stage": "SST_DESKEW_IMAGE",
    "DeskewMode": {
        "ContentDirection": 0,
        "Mode": "DSM_PERSPECTIVE_CORRECTION"
    },
    "PageSize": [-1, -1]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for deskewing images.
> - To use it, add this object to the `StageArray` within a [DocumentDeskewingSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-deskewing.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_DESKEW_IMAGE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_DESKEW_IMAGE"` |

### DeskewMode

Specifies the method in which the deskew process is applied to the target image. See [`DeskewMode`](deskew-mode.md) for details.

### PageSize

Sets the page size (width by height in pixels) of the image after deskew process. See [`PageSize`](page-size.md) for details.