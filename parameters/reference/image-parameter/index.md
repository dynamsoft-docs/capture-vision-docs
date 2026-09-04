---
layout: default-layout
title: ImageParameter Parameters - Dynamsoft Capture Vision
description: Reference index for ImageParameter object in Dynamsoft Capture Vision parameters, covering image processing stages including grayscale conversion, binarization, texture detection, text zone detection, and shortline detection.
keywords: ImageParameter, image processing, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# ImageParameter Parameters

The `ImageParameter` object configures parameters for image processing stages in Dynamsoft Capture Vision, including grayscale conversion, enhancement, binarization, texture detection, and more.

## Example JSON

```json
{
    "ImageParameterOptions": [
        {
            "Name": "ip_default",
            "BaseImageParameterName": "",
            "ApplicableStages": [
                {
                    "Stage": "SST_CONVERT_TO_GRAYSCALE",
                    "ColourConversionModes": []
                },
                {
                    "Stage": "SST_BINARIZE_IMAGE",
                    "BinarizationModes": []
                },
                {
                    "Stage": "SST_SCALE_IMAGE",
                    "ImageScaleSettings": {
                        "ScaledDownThreshold": 2300,
                        "ScaledUpThreshold": 500
                    }
                }
            ]
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `ImageParameter` object inside `ImageParameterOptions`.

`ApplicableStages` defines stage objects. Stage-scoped parameters are constrained by the `Stage` value in each item.

```text
ImageParameter
├── Name
├── BaseImageParameterName
└── ApplicableStages[]
  └── item
    ├── Stage
    └── stage-scoped parameters
      ├── BinarizationModes
      ├── ColourConversionModes
      ├── GrayscaleEnhancementModes
      ├── GrayscaleTransformationModes
      ├── RegionPredetectionModes
      ├── TextDetectionMode
      ├── TextureDetectionModes
      ├── ShortlineDetectionMode
      ├── LineAssemblyMode
      ├── IfEraseTextZone
      └── ImageScaleSettings
```

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the ImageParameter object. |
| [`BaseImageParameterName`](base-image-parameter-name.md) | The name of another ImageParameter to inherit from. |
| [`ApplicableStages`](applicable-stages.md) | The stages that this ImageParameter applies to. |

## Nested Parameter Quick Links

### Actual Nested Parameters in the Tree

| Parameter Name | Description |
|:---------------|:------------|
| [`BinarizationModes`](binarization-modes.md) | The modes for image binarization. |
| [`ColourConversionModes`](colour-conversion-modes.md) | The modes for colour-to-grayscale conversion. |
| [`GrayscaleEnhancementModes`](grayscale-enhancement-modes.md) | The modes for grayscale enhancement. |
| [`GrayscaleTransformationModes`](grayscale-transformation-modes.md) | The modes for grayscale transformation. |
| [`IfEraseTextZone`](if-erase-text-zone.md) | Whether to erase text zones. |
| [`ImageScaleSettings`](image-scale-settings.md) | The settings for image scaling. |
| [`LineAssemblyMode`](line-assembly-mode.md) | The mode for line assembly. |
| [`RegionPredetectionModes`](region-predetection-modes.md) | The modes for region predetection. |
| [`ShortlineDetectionMode`](shortline-detection-mode.md) | The mode for shortline detection. |
| [`TextDetectionMode`](text-detection-mode.md) | The mode for text detection. |
| [`TextureDetectionModes`](texture-detection-modes.md) | The modes for texture detection. |

### Conceptual Stage Objects

| Object | Description |
|:-------|:------------|
| [`StageInputColorImage`](stage-input-color-image.md) | Stage object with `Stage = SST_INPUT_COLOR_IMAGE`. |
| [`StageConvertToGrayscale`](stage-convert-to-grayscale.md) | Stage object with `Stage = SST_CONVERT_TO_GRAYSCALE`. |
| [`StageTransformGrayscale`](stage-transform-grayscale.md) | Stage object with `Stage = SST_TRANSFORM_GRAYSCALE`. |
| [`StageEnhanceGrayscale`](stage-enhance-grayscale.md) | Stage object with `Stage = SST_ENHANCE_GRAYSCALE`. |
| [`StageBinarizeImage`](stage-binarize-image.md) | Stage object with `Stage = SST_BINARIZE_IMAGE`. |
| [`StageDetectTexture`](stage-detect-texture.md) | Stage object with `Stage = SST_DETECT_TEXTURE`. |
| [`StageRemoveTextureFromGrayscale`](stage-remove-texture-from-grayscale.md) | Stage object with `Stage = SST_REMOVE_TEXTURE_FROM_GRAYSCALE`. |
| [`StageBinarizeTextureRemovedGrayscale`](stage-binarize-texture-removed-grayscale.md) | Stage object with `Stage = SST_BINARIZE_TEXTURE_REMOVED_GRAYSCALE`. |
| [`StageDetectTextZones`](stage-detect-text-zones.md) | Stage object with `Stage = SST_DETECT_TEXT_ZONES`. |
| [`StageRemoveTextZonesFromBinary`](stage-remove-text-zones-from-binary.md) | Stage object with `Stage = SST_REMOVE_TEXT_ZONES_FROM_BINARY`. |
| [`StageDetectShortlines`](stage-detect-shortlines.md) | Stage object with `Stage = SST_DETECT_SHORTLINES`. |
| [`StageFindContours`](stage-find-contours.md) | Stage object with `Stage = SST_FIND_CONTOURS`. |
| [`StageAssembleLines`](stage-assemble-lines.md) | Stage object with `Stage = SST_ASSEMBLE_LINES`. |
| [`StageScaleImage`](stage-scale-image.md) | Stage object with `Stage = SST_SCALE_IMAGE`. |


