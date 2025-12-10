---
layout: default-layout
title: RemoveTextureFromGrayscaleStage - Dynamsoft Capture Vision Parameters
description: The RemoveTextureFromGrayscaleStage removes texture from the grayscale image.
keywords: Remove Texture from Grayscale Stage
---

# RemoveTextureFromGrayscaleStage

`RemoveTextureFromGrayscaleStage` removes texture from the grayscale image. In JSON, it is represented as a Stage object with `"Stage": "SST_REMOVE_TEXTURE_FROM_GRAYSCALE"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_REMOVE_TEXTURE_FROM_GRAYSCALE")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_REMOVE_TEXTURE_FROM_GRAYSCALE",
    "TextureRemovalStrength": 2
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for removing texture from grayscale images.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_REMOVE_TEXTURE_FROM_GRAYSCALE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_REMOVE_TEXTURE_FROM_GRAYSCALE"` |

### TextureRemovalStrength

Defines the strength for removing texture from the grayscale image.

| Parameter Details |
| :------------- |
| **Type**<br>*int* |
| **Value Range**<br>[1, 9] |
| **Default Value**<br>2 for BarcodeReaderTask & DocumentNormalizerTask<br>1 for LabelRecognizerTask |
