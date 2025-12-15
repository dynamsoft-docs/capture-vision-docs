---
layout: default-layout
title: ImageParameter - Dynamsoft Capture Vision Parameter File
description: ImageParameter in the Dynamsoft Capture Vision Parameter File is an object for configuring common image processing steps.
keywords: image parameter, image processing, setting
---

# ImageParameter Object

The `ImageParameter` object is designed to configure and organize parameters for image processing stages, including convert color-to-grayscale, enhance grayscale, binarize image, detect text zones, and detect texture stages. You can configure detailed parameters for each stage.

## Example

```json
{
    "ImageParameterOptions": [
        {
            "Name": "ip_default",
            "BaseImageParameterName": "ip_base",
            "ApplicableStages": [
                {"Stage": "SST_SCALE_IMAGE", "ImageScaleSetting": {}},
                {"Stage": "SST_CONVERT_TO_GRAYSCALE", "ColourConversionModes": []},
                {"Stage": "SST_TRANSFORM_GRAYSCALE", "GrayscaleTransformationModes": []},
                {"Stage": "SST_ENHANCE_GRAYSCALE", "GrayscaleEnhancementModes": []},
                {"Stage": "SST_BINARIZE_IMAGE", "BinarizationModes": []},
                {"Stage": "SST_DETECT_TEXTURE", "TextureDetectionModes": []},
                {"Stage": "SST_REMOVE_TEXTURE_FROM_GRAYSCALE"},
                {"Stage": "SST_BINARIZE_TEXTURE_REMOVED_GRAYSCALE"},
                {"Stage": "SST_FIND_CONTOURS"},
                {"Stage": "SST_DETECT_SHORTLINES", "ShortlineDetectionMode": {}},
                {"Stage": "SST_ASSEMBLE_LINES", "LineAssemblyMode": {}},
                {"Stage": "SST_DETECT_TEXT_ZONES", "TextDetectionMode": {}},
                {"Stage": "SST_REMOVE_TEXT_ZONES_FROM_BINARY", "IfEraseTextZone": 0}
            ]
        }
    ]
}
```

## Parameters

| Parameter Name | Type | Required/Optional | Description |
| -------------- | ---- | ----------------- | ----------- |
| [`Name`]({{site.dcvb_parameters_reference}}image-parameter/name.html) | String | Required | The unique identifier for this `ImageParameter` object. |
| [`BaseImageParameterName`]({{site.dcvb_parameters_reference}}image-parameter/base-image-parameter-name.html) | String | Optional | The name of another `ImageParameter` object to inherit settings from. |
| [`ApplicableStages`]({{site.dcvb_parameters_reference}}image-parameter/applicable-stages.html) | Array | Optional | An array of stage objects defining the image processing pipeline. |

## Usage

Each functional product has default `ImageParameter` settings. You can either use the defaults or define custom `ImageParameter` objects for specific sections.

### Defining ImageParameter Objects

`ImageParameter` objects are configured under `ImageParameterOptions`, each with a unique name:

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

You can create a new `ImageParameter` based on an existing one using inheritance:

```json
{
    "ImageParameterOptions": [
        {
            "Name": "IP_0"
        },
        {
            "Name": "IP_1",
            "BaseImageParameterName": "IP_0"
        }
    ]
}
```

### Referencing in Task Settings

Reference `ImageParameter` objects in task settings by name:

```json
{
    "SectionArray": [
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

## Available Stages

| Stage Name | Description |
| ---------- | ----------- |
| [`SST_SCALE_IMAGE`]({{site.dcvb_parameters_reference}}image-parameter/stage-scale-image.html) | Scales the image up or down. |
| [`SST_CONVERT_TO_GRAYSCALE`]({{site.dcvb_parameters_reference}}image-parameter/stage-convert-to-grayscale.html) | Converts a color image to grayscale. |
| [`SST_TRANSFORM_GRAYSCALE`]({{site.dcvb_parameters_reference}}image-parameter/stage-transform-grayscale.html) | Transforms the grayscale image (e.g., for inverted barcodes). |
| [`SST_ENHANCE_GRAYSCALE`]({{site.dcvb_parameters_reference}}image-parameter/stage-enhance-grayscale.html) | Enhances grayscale image quality. |
| [`SST_BINARIZE_IMAGE`]({{site.dcvb_parameters_reference}}image-parameter/stage-binarize-image.html) | Converts grayscale to binary image. |
| [`SST_DETECT_TEXTURE`]({{site.dcvb_parameters_reference}}image-parameter/stage-detect-texture.html) | Detects texture patterns in the image. |
| [`SST_REMOVE_TEXTURE_FROM_GRAYSCALE`]({{site.dcvb_parameters_reference}}image-parameter/stage-remove-texture-from-grayscale.html) | Removes texture from grayscale image. |
| [`SST_BINARIZE_TEXTURE_REMOVED_GRAYSCALE`]({{site.dcvb_parameters_reference}}image-parameter/stage-binarize-texture-removed-grayscale.html) | Binarizes the texture-removed grayscale image. |
| [`SST_FIND_CONTOURS`]({{site.dcvb_parameters_reference}}image-parameter/stage-find-contours.html) | Finds contours in the image. |
| [`SST_DETECT_SHORTLINES`]({{site.dcvb_parameters_reference}}image-parameter/stage-detect-shortlines.html) | Detects short lines for document boundary detection. |
| [`SST_ASSEMBLE_LINES`]({{site.dcvb_parameters_reference}}image-parameter/stage-assemble-lines.html) | Assembles detected lines. |
| [`SST_DETECT_TEXT_ZONES`]({{site.dcvb_parameters_reference}}image-parameter/stage-detect-text-zones.html) | Detects text zones in the image. |
| [`SST_REMOVE_TEXT_ZONES_FROM_BINARY`]({{site.dcvb_parameters_reference}}image-parameter/stage-remove-text-zones-from-binary.html) | Removes text zones from binary image. |

## Stage Parameters

Each stage can have associated parameters for fine-tuning:

- **SST_SCALE_IMAGE**: [`ImageScaleSetting`]({{site.dcvb_parameters_reference}}image-parameter/image-scale-settings.html)
- **SST_CONVERT_TO_GRAYSCALE**: [`ColourConversionModes`]({{site.dcvb_parameters_reference}}image-parameter/colour-conversion-modes.html)
- **SST_TRANSFORM_GRAYSCALE**: [`GrayscaleTransformationModes`]({{site.dcvb_parameters_reference}}image-parameter/grayscale-transformation-modes.html)
- **SST_ENHANCE_GRAYSCALE**: [`GrayscaleEnhancementModes`]({{site.dcvb_parameters_reference}}image-parameter/grayscale-enhancement-modes.html)
- **SST_BINARIZE_IMAGE**: [`BinarizationModes`]({{site.dcvb_parameters_reference}}image-parameter/binarization-modes.html)
- **SST_DETECT_TEXTURE**: [`TextureDetectionModes`]({{site.dcvb_parameters_reference}}image-parameter/texture-detection-modes.html)
- **SST_DETECT_SHORTLINES**: [`ShortlineDetectionMode`]({{site.dcvb_parameters_reference}}image-parameter/shortline-detection-mode.html)
- **SST_ASSEMBLE_LINES**: [`LineAssemblyMode`]({{site.dcvb_parameters_reference}}image-parameter/line-assembly-mode.html)
- **SST_DETECT_TEXT_ZONES**: [`TextDetectionMode`]({{site.dcvb_parameters_reference}}image-parameter/text-detection-mode.html)
- **SST_REMOVE_TEXT_ZONES_FROM_BINARY**: [`IfEraseTextZone`]({{site.dcvb_parameters_reference}}image-parameter/if-erase-text-zone.html)
