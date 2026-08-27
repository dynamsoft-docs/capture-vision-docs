---
layout: default-layout
title: ImageParameter Parameters - Dynamsoft Capture Vision
description: Reference index for ImageParameter parameters in Dynamsoft Capture Vision, covering image processing stages including grayscale conversion, binarization, texture detection, text zone detection, and shortline detection.
keywords: ImageParameter, image processing, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# ImageParameter Parameters

The `ImageParameter` object configures parameters for image processing stages in Dynamsoft Capture Vision, including grayscale conversion, enhancement, binarization, texture detection, and more.

## General

| Parameter | Description |
|:----------|:------------|
| [`Name`](name.html) | The unique name of the ImageParameter object. |
| [`BaseImageParameterName`](base-image-parameter-name.html) | The name of another ImageParameter to inherit from. |
| [`ApplicableStages`](applicable-stages.html) | The stages that this ImageParameter applies to. |

## Processing Modes

| Parameter | Description |
|:----------|:------------|
| [`BinarizationModes`](binarization-modes.html) | The modes for image binarization. |
| [`ColourConversionModes`](colour-conversion-modes.html) | The modes for colour-to-grayscale conversion. |
| [`GrayscaleEnhancementModes`](grayscale-enhancement-modes.html) | The modes for grayscale enhancement. |
| [`GrayscaleTransformationModes`](grayscale-transformation-modes.html) | The modes for grayscale transformation. |
| [`RegionPredetectionModes`](region-predetection-modes.html) | The modes for region predetection. |
| [`TextDetectionMode`](text-detection-mode.html) | The mode for text detection. |
| [`TextureDetectionModes`](texture-detection-modes.html) | The modes for texture detection. |
| [`ShortlineDetectionMode`](shortline-detection-mode.html) | The mode for shortline detection. |
| [`LineAssemblyMode`](line-assembly-mode.html) | The mode for line assembly. |
| [`IfEraseTextZone`](if-erase-text-zone.html) | Whether to erase text zones. |
| [`ImageScaleSettings`](image-scale-settings.html) | The settings for image scaling. |

## Stage Configuration

| Parameter | Description |
|:----------|:------------|
| [`StageInputColorImage`](stage-input-color-image.html) | Stage for inputting color images. |
| [`StageConvertToGrayscale`](stage-convert-to-grayscale.html) | Stage for converting to grayscale. |
| [`StageTransformGrayscale`](stage-transform-grayscale.html) | Stage for transforming grayscale. |
| [`StageEnhanceGrayscale`](stage-enhance-grayscale.html) | Stage for enhancing grayscale. |
| [`StageBinarizeImage`](stage-binarize-image.html) | Stage for binarizing images. |
| [`StageDetectTexture`](stage-detect-texture.html) | Stage for detecting texture. |
| [`StageRemoveTextureFromGrayscale`](stage-remove-texture-from-grayscale.html) | Stage for removing texture from grayscale. |
| [`StageBinarizeTextureRemovedGrayscale`](stage-binarize-texture-removed-grayscale.html) | Stage for binarizing texture-removed grayscale. |
| [`StageDetectTextZones`](stage-detect-text-zones.html) | Stage for detecting text zones. |
| [`StageRemoveTextZonesFromBinary`](stage-remove-text-zones-from-binary.html) | Stage for removing text zones from binary. |
| [`StageDetectShortlines`](stage-detect-shortlines.html) | Stage for detecting shortlines. |
| [`StageFindContours`](stage-find-contours.html) | Stage for finding contours. |
| [`StageAssembleLines`](stage-assemble-lines.html) | Stage for assembling lines. |
| [`StageScaleImage`](stage-scale-image.html) | Stage for scaling images. |
