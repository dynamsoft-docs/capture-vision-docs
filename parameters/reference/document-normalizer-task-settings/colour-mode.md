---
layout: default-layout
title: ColourMode - Dynamsoft Document Normalizer Parameters
description: The parameter ColourMode defines the output colour mode of the image.
keywords: ColourMode
---

# ColourMode

`ColourMode` defines the output colour mode of the target image. It influences the image that output by both `CapturedResult` and `IntermediateResult`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_ENHANCE_IMAGE")
            └── ColourMode
```

**Parent object:** [EnhanceImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-enhance-image.html)

**Example:**

```json
{
    "ColourMode": "ICM_GRAYSCALE"
}
```

> [!NOTE]
> - This snippet shows only the `ColourMode` parameter.
> - To use it, embed this parameter within an [EnhanceImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-enhance-image.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| ColourMode Parameter Details |
| :--------------------------- |
| **Type**<br>*String* |
| **Available Colour Mode List**<br><br>ICM_BINARY<br>ICM_GRAYSCALE<br>ICM_COLOUR |
| **Default Value**<br>"ICM_COLOUR" |
