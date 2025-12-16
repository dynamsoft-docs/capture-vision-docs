---
layout: default-layout
title: PageSize - Dynamsoft Document Normalizer Parameters
description: The parameter PageSize sets the page size of the target image.
keywords: Page size
---

# PageSize

`PageSize` sets the page size (width by height in pixels) of the target image.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_DESKEW_IMAGE")
            └── PageSize
```

**Parent object:** [DeskewImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-deskew-image.html)

**Example:**

```json
{
    "PageSize": [210, 297]
}
```

> [!NOTE]
> - This snippet shows only the `PageSize` parameter.
> - To use it, embed this parameter within a [DeskewImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-deskew-image.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| PageSize Parameter Details |
| :--------------- |
| **Type**<br><i>int[2]</i> |
| **Range**<br>Each member should be a int value betweem [-1,0x7fffffff]. |
| **Default Value**<br>[-1,-1] |
| **Remarks**<br>A page size is defined as: [TargetPageWidth, TargetPageHeight].<br>TargetPageWidth * TargetPageHeight < 100000000.<br>If any of TargetPageWidth and TargetPageHeight is 0 or -1, the original width and height of the detected content will be used. |
