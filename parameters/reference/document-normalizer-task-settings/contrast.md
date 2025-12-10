---
layout: default-layout
title: Contrast - Dynamsoft Document Normalizer Parameters
description: The parameter Contrast specifies the contrast of the image.
keywords: Contrast
---

# Contrast

`Contrast` specifies the contrast of the image.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_ENHANCE_IMAGE")
            └── Contrast
```

**Parent object:** [EnhanceImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-enhance-image.html)

**Example:**

```json
{
    "Contrast": 0
}
```

> [!NOTE]
> - This snippet shows only the `Contrast` parameter.
> - To use it, embed this parameter within an [EnhanceImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-enhance-image.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Contrast Parameter Details |
| :------------------------ |
| **Type**<br>*int* |
| **Range**<br>[-100,100] |
| **Default Value**<br>0 |
