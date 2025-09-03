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

The ImageParameter object is designed to configure and organize common parameters for image processing, including but not limited to color-to-grayscale conversion, grayscale enhancement, binarization, color region pre-detection, text detection, and texture detection. These configuration parameters play a role in different stages of recognition tasks.

```json
{
    "Name" : "ip_default",
    "BaseImageParameterName" : "",
    "BinarizationModes" : 
    [
        {
            "BinarizationThreshold" : -1,
            "BlockSizeX" : 0,
            "BlockSizeY" : 0,
            "EnableFillBinaryVacancy" : 1,
            "GrayscaleEnhancementModesIndex" : -1,
            "Mode" : "BM_LOCAL_BLOCK",
            "MorphOperation" : "Close",
            "MorphOperationKernelSizeX" : -1,
            "MorphOperationKernelSizeY" : -1,
            "MorphShape" : "Rectangle",
            "ThresholdCompensation" : 10
        }
    ],
    "ColourConversionModes" : 
    [
        {
            "BlueChannelWeight" : -1,
            "GreenChannelWeight" : -1,
            "Mode" : "CICM_GENERAL",
            "RedChannelWeight" : -1,
            "ReferChannel" : "H_CHANNEL"
        }
    ],
    "GrayscaleEnhancementModes" : 
    [
        {
            "Mode" : "GEM_GENERAL",
            "Sensitivity" : -1,
            "SharpenBlockSizeX" : -1,
            "SharpenBlockSizeY" : -1,
            "SmoothBlockSizeX" : -1,
            "SmoothBlockSizeY" : -1
        }
    ],
    "GrayscaleTransformationModes" : 
    [
        {
            "Mode" : "GTM_ORIGINAL"
        }
    ],
    "IfEraseTextZone" : 0,
    "RegionPredetectionModes" : 
    [
        {
            "AspectRatioRange" : "[]",
            "FindAccurateBoundary" : 0,
            "ForeAndBackgroundColours" : "[]",
            "HeightRange" : "[]",
            "ImageParameterName" : "",
            "MeasuredByPercentage" : 1,
            "MinImageDimension" : 262144,
            "Mode" : "RPM_GENERAL",
            "RelativeRegions" : "[]",
            "Sensitivity" : 1,
            "SpatialIndexBlockSize" : 5,
            "WidthRange" : "[]"
        }
    ],
    "ScaleDownThreshold" : 2300,
    "ScaleUpModes" : 
    [
        {
            "AcuteAngleWithXThreshold" : -1,
            "LetterHeightThreshold" : 0,
            "Mode" : "SUM_AUTO",
            "ModuleSizeThreshold" : 0,
            "TargetLetterHeight" : 0,
            "TargetModuleSize" : 0
        }
    ],
    "TextDetectionMode" : 
    {
        "CharHeightRange" : 
        [
            1,
            1000,
            1
        ],
        "Direction" : "HORIZONTAL",
        "MaxSpacingInALine" : -1,
        "Mode" : "TTDM_SKIP"
    },
    "TextureDetectionModes" : 
    [
        {
            "Mode" : "TDM_GENERAL_WIDTH_CONCENTRATION",
            "Sensitivity" : 5
        }
    ]
}
```

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
    "SectionImageParameterArray":
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
| -------------- | ----------- |
| [`Name`](../reference/shared-parameter/name.md) | Represents the name of the `ImageParameter` object, which serves as its unique identifier. |
| [`BaseImageParameterName`](../reference/image-parameter/base-image-parameter-name.md) | Represents the name of another `ImageParameter` object. It is used to inherit the parameters defined in its parent `ImageParameter` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.|
| [`BinarizationModes`](../reference/image-parameter/binarization-modes.md) | Used to control the binarization process, including two modes of local binarization and global binarization. |
| [`ColourConversionModes`](../reference/image-parameter/colour-conversion-modes.md) | Used to control the process of colour conversion, i.e. converting a colour image to a grayscale image.|
| [`GrayscaleEnhancementModes`](../reference/image-parameter/grayscale-enhancement-modes.md) | Provides some image processing methods to enhance the quality of the grayscale image, including gray equalization, grayscale smoothing, grayscale sharpening and smoothing.|
| [`GrayscaleTransformationModes`](../reference/image-parameter/grayscale-transformation-modes.md) | Used to control the color mode of the grayscale image, including the original mode and the inverted mode. |
| [`IfEraseTextZone`](../reference/image-parameter/if-erase-text-zone.md) | Indicates whether to erase the detected text area in the image.|
| [`RegionPredetectionModes`](../reference/image-parameter/region-predetection-modes.md) | Controls how to find a region of interest (ROI) within the image or frame. It consists of one or more modes, each mode representing a different way to find a region of interest.|
| [`ScaleDownThreshold`](../reference/image-parameter/scale-down-threshold.md) | Controls the threshold used when shrinking an image. If the shorter edge size is larger than the given value, the library will calculate the required height and width of the image and shrink the image to that size.|
| [`ScaleUpModes`](../reference/image-parameter/scale-up-modes.md)| Determines the process for scaling up an image used for detecting barcodes with small module size or recognizing text lines with small fonts. It consists of one or more modes, each mode represents a way to implement the scale-up. |
| [`TextDetectionMode`](../reference/image-parameter/text-detection-mode.md) | Determines how to detect texts on an image. It consists of one or more modes, each mode represents a way to implement the detection. |
| [`TextureDetectionModes`](../reference/image-parameter/texture-detection-modes.md) | Determines how to detect texture on an image. It consists of one or more modes, each mode represents a way to implement the detection. |
