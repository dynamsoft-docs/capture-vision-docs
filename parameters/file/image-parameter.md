---
layout: default-layout
title: ImageParameter - Dynamsoft Capture Vision Parameter File
description: ImageParameter in the Dynamsoft Capture Vision Parameter File is an object for configuring common image processing steps.
keywords: image parameter, image processing, setting
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
---

# ImageParameter Object

The ImageParameter object is designed to configure and organize parameters for image processing stages, including but not limited to convert color-to-grayscale stage, enhance grayscale image stage, binarize image stage, detect text zone stage, and detect texture stage. You can configure detailed parameters for each stage.

```json
"ImageParameterOptions": [
    {
        "Name" : "ip_default",
        "BaseImageParameterName": "ip_base",
        "ApplicableStages":[
            { "Stage": "SST_SCALE_IMAGE", "ImageScaleSetting" : {} },
            { "Stage": "SST_CONVERT_TO_GRAYSCALE", "ColourConversionModes" : [] },
            { "Stage": "SST_TRANSFORM_GRAYSCALE", "GrayscaleTransformationModes" : [] },
            { "Stage": "SST_ENHANCE_GRAYSCALE", "GrayscaleEnhancementModes" : [] },
            { "Stage": "SST_BINARIZE_IMAGE", "BinarizationModes" : [] },
            { "Stage": "SST_DETECT_TEXTURE", "TextureDetectionModes" : [] },
            { "Stage": "SST_REMOVE_TEXTURE_FROM_GRAYSCALE" },
            { "Stage": "SST_BINARIZE_TEXTURE_REMOVED_GRAYSCALE" },
            { "Stage": "SST_FIND_CONTOURS" },
            { "Stage": "SST_DETECT_SHORTLINES", "ShortlineDetectionMode": {} },
            { "Stage": "SST_ASSEMBLE_LINES", "LineAssemblyMode": {} },
            { "Stage": "SST_DETECT_TEXT_ZONES", "TextDetectionMode": {} },
            { "Stage": "SST_REMOVE_TEXT_ZONES_FROM_BINARY", "IfEraseTextZone": 0 }
        ]
    }
],
```

- [Name]({{ site.dcvb_parameters_reference }}image-parameter/name.html)
- [BaseImageParameterName]({{ site.dcvb_parameters_reference }}image-parameter/base-image-parameter-name.html)
- [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html)
  - [Scale Image Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-scale-image.html)
    - [ImageScaleSetting]({{ site.dcvb_parameters_reference }}image-parameter/image-scale-settings.html)
  - [Convert to Grayscale Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-convert-to-grayscale.html)
    - [ColourConversionModes]({{ site.dcvb_parameters_reference }}image-parameter/colour-conversion-modes.html)
  - [Transform Grayscale Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-transform-grayscale.html)
    - [GrayscaleTransformationModes]({{ site.dcvb_parameters_reference }}image-parameter/grayscale-transformation-modes.html)
  - [Enhance Grayscale Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-enhance-grayscale.html)
    - [GrayscaleEnhancementModes]({{ site.dcvb_parameters_reference }}image-parameter/grayscale-enhancement-modes.html)
  - [Binarize Image Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-binarize-image.html)
    - [BinarizationModes]({{ site.dcvb_parameters_reference }}image-parameter/binarization-modes.html)
  - [Detect Texture Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-detect-texture.html)
    - [TextureDetectionModes]({{ site.dcvb_parameters_reference }}image-parameter/texture-detection-modes.html)
  - [Remove Texture From Grayscale Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-remove-texture-from-grayscale.html)
  - [Binarize Texture Removed Grayscale Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-binarize-texture-removed-grayscale.html)
  - [Find Contours Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-find-contours.html)
  - [Detect Shortlines Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-detect-shortlines.html)
    - [ShortlineDetectionMode]({{ site.dcvb_parameters_reference }}image-parameter/shortline-detection-mode.html)
  - [Assemble Lines Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-assemble-lines.html)
    - [LineAssemblyMode]({{ site.dcvb_parameters_reference }}image-parameter/line-assembly-mode.html)
  - [Detect Text Zones Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-detect-text-zones.html)
    - [TextDetectionMode]({{ site.dcvb_parameters_reference }}image-parameter/text-detection-mode.html)
  - [Remove Text Zones From Binary Stage]({{ site.dcvb_parameters_reference }}image-parameter/stage-remove-text-zones-from-binary.html)
    - [IfEraseTextZone]({{ site.dcvb_parameters_reference }}image-parameter/if-erase-text-zone.html)

## Definition and Reference

Each algorithm section of the funtional products has a default `ImageParameter` settings. You can either skip the ImageParameter settings to implement the default settings or define your own `ImageParameter` objects and specify them in the sections you want to customize.

### Define an ImageParameter Object

`ImageParameter` objects are configured under `ImageParameterOptions` and each object has a unique name as its identifier.

```json
{
    "ImageParameterOptions": [
        {
            "Name": "IP_0"
        },
        {
            "Name": "IP_1"
        }
    ]
}
```

You can define a new `ImageParameter` object based on an existing `ImageParameter` object. For example:

```json
{
    "ImageParameterOptions": [
        {
            "Name": "IP_0"
        },
        {
            "Name": "IP_1",
            "BaseImageParameterName" : "IP_0"
        }
    ]
}
```

### Specify an ImageParameter for Task Sections

`ImageParameter` is referenced in task settings under `SectionImageParameterArray` with their names. For example:

```json
{
    "SectionArray":
    [
        {
            "Section": "ST_REGION_PREDETECTION",
            "ImageParameterName": "IP_0"
        },
        {
            "Section": "ST_BARCODE_LOCALIZATION",
            "ImageParameterName": "IP_1"
        },
        {
            "Section": "ST_BARCODE_DECODING",
            "ImageParameterName": "IP_2"
        }
    ]
}
```

## Summary of ImageParameter Top-level Parameters

View the parameter references for the details of each `ImageParameter` parameters.

| Parameter Name | Description |
| ---------------------------------- | ----------- |
| [`BaseImageParameterName`](../reference/image-parameter/base-image-parameter-name.md) | Represents the name of another `ImageParameter` object to inherit from. |
| [`Name`](../reference/image-parameter/name.md) | Defines the name of a `ImageParameter` object, which serves as its unique identifier. |
| [`ApplicableStages`](../reference/image-parameter/applicable-stages.md) | Defines the applicable stage parameters with an array of stage objects. |

## Available Stages

| Stage Name | Description |
| ---------- | ----------- |
| [`SST_SCALE_IMAGE`](../reference/image-parameter/stage-scale-image.md) | The stage for scaling up or down the image. |
| [`SST_CONVERT_TO_GRAYSCALE`](../reference/image-parameter/stage-convert-to-grayscale.md) | The stage for converting a colour image to a grayscale image. |
| [`SST_TRANSFORM_GRAYSCALE`](../reference/image-parameter/stage-transform-grayscale.md) | The stage for transforming the grayscale image. Generally used when processing inverted barcodes or text lines. |
| [`SST_ENHANCE_GRAYSCALE`](../reference/image-parameter/stage-enhance-grayscale.md) | The stage for enhancing the quality of the grayscale image. |
| [`SST_BINARIZE_IMAGE`](../reference/image-parameter/stage-binarize-image.md) | The stage for binarizing the image. |
| [`SST_DETECT_TEXTURE`](../reference/image-parameter/stage-detect-texture.md) | The stage for detecting texture on the image. |
| [`SST_REMOVE_TEXTURE_FROM_GRAYSCALE`](../reference/image-parameter/stage-remove-texture-from-grayscale.md) | The stage for removing texture from the grayscale image. |
| [`SST_BINARIZE_TEXTURE_REMOVED_GRAYSCALE`](../reference/image-parameter/stage-binarize-texture-removed-grayscale.md) | The stage for binarizing the texture removed grayscale image. |
| [`SST_FIND_CONTOURS`](../reference/image-parameter/stage-find-contours.md) | The stage for finding contours in the image. |
| [`SST_DETECT_SHORTLINES`](../reference/image-parameter/stage-detect-shortlines.md) | The stage for detecting short lines for document boundary detection. |
| [`SST_ASSEMBLE_LINES`](../reference/image-parameter/stage-assemble-lines.md) | The stage for assembling lines. |
| [`SST_DETECT_TEXT_ZONES`](../reference/image-parameter/stage-detect-text-zones.md) | The stage for detecting text zones on the image. |
| [`SST_REMOVE_TEXT_ZONES_FROM_BINARY`](../reference/image-parameter/stage-remove-text-zones-from-binary.md) | The stage for removing text zones from the binary image. |
