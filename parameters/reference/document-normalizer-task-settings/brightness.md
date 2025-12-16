---
layout: default-layout
title: Brightness - Dynamsoft Document Normalizer Parameters
description: The parameter Brightness defines the brightness of the image.
keywords: Brightness
---

# Brightness

`Brightness` defines the brightness of the target image.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_ENHANCE_IMAGE")
            └── Brightness
```

**Parent object:** [EnhanceImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-enhance-image.html)

**Example:**

```json
{
    "Brightness": 0
}
```

> [!NOTE]
> - This snippet shows only the `Brightness` parameter.
> - To use it, embed this parameter within an [EnhanceImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-enhance-image.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Brightness Parameter Details |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>[-100, 100] |
| **Default Value**<br>0 |
