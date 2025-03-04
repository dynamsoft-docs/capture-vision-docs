---
layout: default-layout
title: ApplicableStages - Dynamsoft Capture Vision Parameters
description: The parameter ApplicableStages of Dynamsoft Capture Vision is for configuring the applicable stages parameters.
keywords: Stages
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---


# ApplicableStages

Defines the applicable stage parameters with an array of stage objects. Each applicable stage object contains the name of the stage and related parameters.

```json
"ApplicableStages":[
    {
        "Stage":"SST_SCALE_IMAGE",
        "ImageScaleSetting" : {}
    },
    {
        "Stage":"SST_CONVERT_TO_GRAYSCALE",
        "ColourConversionModes" : []
    },
    {
        "Stage":"SST_TRANSFORM_GRAYSCALE",
        "GrayscaleTransformationModes" : []
    },
    {
        "Stage":"SST_ENHANCE_GRAYSCALE",
        "GrayscaleEnhancementModes" : []
    },
]
```

## Stages

| Applicable Name | Descriptions |
| -------------- | ------------ |
| [`SST_ASSEMBLE_LINES`](stage-assemble-lines.md) | The stage that assembles short lines when processing documents. |
| [`SST_BINARIZE_IMAGE`](stage-binarize-image.md) | The stage that transfers a grayscale image into a binary image. |
| [`SST_BINARIZE_TEXTURE_REMOVED_GRAYSCALE`](stage-binarize-texture-removed-grayscale.md) | The stage that transfers a texture-removed grayscale image into a binary image. |
| [`SST_CONVERT_TO_GRAYSCALE`](stage-convert-to-grayscale.md) | The stage that converts a colour image to a grayscale image. |
| [`SST_DETECT_SHORTLINES`](stage-detect-shortlines.md) | The stage that detects short lines for document boundary detection. |
| [`SST_DETECT_TEXTURE`](stage-detect-texture.md) | The stage that detects texture on the image. |
| [`SST_DETECT_TEXT_ZONES`](stage-detect-text-zones.md) | The stage that detects text zones on the image. |
| [`SST_ENHANCE_GRAYSCALE`](stage-enhance-grayscale.md) | The stage that improves the quality of the grayscale image. |
| [`SST_FIND_CONTOURS`](stage-find-contours.md) | The stage that finds contours in the image. |
| [`SST_REMOVE_TEXTURE_FROM_GRAYSCALE`](stage-remove-texture-from-grayscale.md) | The stage that removes texture from the grayscale image. |
| [`SST_REMOVE_TEXT_ZONES_FROM_BINARY`](stage-remove-text-zones-from-binary.md) | The stage that removes text zones from the binary image. |
| [`SST_SCALE_IMAGE`](stage-scale-image.md) | The stage that down/up scales the image. |
| [`SST_TRANSFORM_GRAYSCALE`](stage-transform-grayscale.md) | The stage that transforms the grayscale image. |
