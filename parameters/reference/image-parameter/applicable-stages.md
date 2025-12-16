---
layout: default-layout
title: ApplicableStages - Dynamsoft Capture Vision Parameters
description: The parameter ApplicableStages of Dynamsoft Capture Vision is for configuring the applicable stages parameters.
keywords: ApplicableStages
---


# ApplicableStages

Defines the applicable stage parameters with an array of stage objects. Each applicable stage object contains the name of the stage and related parameters.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages
```

**Parent object:** [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "ApplicableStages": [
        {
            "Stage": "SST_SCALE_IMAGE",
            "ImageScaleSetting": {}
        },
        {
            "Stage": "SST_CONVERT_TO_GRAYSCALE",
            "ColourConversionModes": []
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `ApplicableStages` parameter.
> - To use it, embed this parameter within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The `ImageParameter` includes the following stages:

| Stage Name | Descriptions |
| -------------- | ------------ |
| [AssembleLinesStage](stage-assemble-lines.md) (`SST_ASSEMBLE_LINES`) | The stage that assembles short lines when processing documents. |
| [BinarizeImageStage](stage-binarize-image.md) (`SST_BINARIZE_IMAGE`) | The stage that transfers a grayscale image into a binary image. |
| [BinarizeTextureRemovedGrayscaleStage](stage-binarize-texture-removed-grayscale.md) (`SST_BINARIZE_TEXTURE_REMOVED_GRAYSCALE`) | The stage that transfers a texture-removed grayscale image into a binary image. |
| [ConvertToGrayscaleStage](stage-convert-to-grayscale.md) (`SST_CONVERT_TO_GRAYSCALE`) | The stage that converts a colour image to a grayscale image. |
| [DetectShortLinesStage](stage-detect-shortlines.md) (`SST_DETECT_SHORTLINES`) | The stage that detects short lines for document boundary detection. |
| [DetectTextureStage](stage-detect-texture.md) (`SST_DETECT_TEXTURE`) | The stage that detects texture on the image. |
| [DetectTextZonesStage](stage-detect-text-zones.md) (`SST_DETECT_TEXT_ZONES`) | The stage that detects text zones on the image. |
| [EnhanceGrayscaleStage](stage-enhance-grayscale.md) (`SST_ENHANCE_GRAYSCALE`) | The stage that improves the quality of the grayscale image. |
| [FindContoursStage](stage-find-contours.md) (`SST_FIND_CONTOURS`) | The stage that finds contours in the image. |
| [RemoveTextureFromGrayscaleStage](stage-remove-texture-from-grayscale.md) (`SST_REMOVE_TEXTURE_FROM_GRAYSCALE`) | The stage that removes texture from the grayscale image. |
| [RemoveTextZonesFromBinaryStage](stage-remove-text-zones-from-binary.md) (`SST_REMOVE_TEXT_ZONES_FROM_BINARY`) | The stage that removes text zones from the binary image. |
| [ScaleImageStage](stage-scale-image.md) (`SST_SCALE_IMAGE`) | The stage that down/up scales the image. |
| [TransformGrayscaleStage](stage-transform-grayscale.md) (`SST_TRANSFORM_GRAYSCALE`) | The stage that transforms the grayscale image. |
