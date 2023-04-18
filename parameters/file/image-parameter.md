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
    "ColourChannelUsageType" : "CCUT_AUTO",
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
    "Name" : "ip_default",
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

## Summary of ImageParameter top-level parameters

| Parameter Name | Description |
| -------------- | ----------- |
| `Name` | Represents the name of the `ImageParameter` object, which serves as its unique identifier. |
| `BaseImageParameterName` | Represents the name of another `ImageParameter` object. It is used to inherit the parameters defined in its parent `ImageParameter` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.|
| `BinarizationModes` | Used to control the binarization process, including two modes of local binarization and global binarization. |
| `ColourChannelUsageType` | Specifies how to use the colour channel from the source image buffer.|
| `ColourConversionModes` | Used to control the process of colour conversion, i.e. converting a colour image to a grayscale image.|
| `GrayscaleEnhancementModes` | Provides some image processing methods to enhance the quality of the grayscale image, including gray equalization, grayscale smoothing, grayscale sharpening and smoothing.|
| `GrayscaleTransformationModes` | Used to control the color mode of the grayscale image, including the original mode and the inverted mode. |
| `IfEraseTextZone` | Indicates whether to erase the detected text area in the image.|
| `RegionPredetectionModes` | Controls how to find a region of interest (ROI) within the image or frame. It consists of one or more modes, each mode representing a different way to find a region of interest.|
| `ScaleDownThreshold` | Controls the threshold used when shrinking an image. If the shorter edge size is larger than the given value, the library will calculate the required height and width of the image and shrink the image to that size.|
| `ScaleUpModes`| Determines the process for scaling up an image used for detecting barcodes with small module size or recognizing text lines with small fonts. It consists of one or more modes, each mode represents a way to implement the scale-up. |
| `TextDetectionMode` | Determines how to detect texts on an image. It consists of one or more modes, each mode represents a way to implement the detection. |
| `TextureDetectionModes` | Determines how to detect texture on an image. It consists of one or more modes, each mode represents a way to implement the detection. |
