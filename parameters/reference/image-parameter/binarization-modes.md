---
layout: default-layout
title: BinarizationModes - Dynamsoft Capture Vision Parameters
description: The parameter BinarizationModes of Dynamsoft Capture Vision is for controlling the process of image binarization.
keywords: BinarizationModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---


# BinarizationModes 

Parameter `BinarizationModes` helps control the process of binarization, i.e., converting a grayscale image to a binary image. A better binary image greatly helps the following processes. During binarization, the threshold is the key criteria. If the pixel value is smaller than the threshold, it is set to 0, otherwise, it is set to a maximum value (255 in the library). By default, the library automatically calculates the adaptive size of the neighbourhood area and then binarizes the grayscale image with the adaptive threshold based on a small neighbourhood area with an adaptive size around it. `BinarizationModes` consists of one or more modes, each mode representing a different binarization process.

## Example

```json
{
    "BinarizationModes" : 
    [
        {
            "BinarizationThreshold" : -1,
            "BlockSizeX" : 0,
            "BlockSizeY" : 0,
            "EnableFillBinaryVacancy" : 1,
            "GrayscaleEnhancementModesIndex" : -1,
            "Mode" : "BM_LOCAL_BLOCK",
            "MorphOperation" : "None",
            "MorphOperationKernelSizeX" : 0,
            "MorphOperationKernelSizeY" : 0,
            "MorphShape" : "Rectangle",
            "ThresholdCompensation" : 10
        }
    ]
}
```

## Parameter Summary

Parameter `BinarizationModes` consist of a group of binarization mode objects. Each binarization mode object includes a candidate mode and a series of mode arguments. The available mode arguments of the binarization mode object is shown as follow.

### Mode Arguments

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Any one in Candidate Mode List as string
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>BM_THRESHOLD
            <br>BM_LOCAL_BLOCK
            <br>BM_AUTO
            <br>BM_SKIP
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">BlockSizeX<br>(Optional)</td>
        <td><b>Description</b><br>Sets the horizontal block size for the binarization process.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,1000]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>BM_LOCAL_BLOCK
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">BlockSizeY<br>(Optional)</td>
        <td><b>Description</b><br>Sets the vertical block size for the binarization process.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,1000]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>BM_LOCAL_BLOCK
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">EnableFillBinaryVacancy<br>(Optional)</td>
        <td><b>Description</b><br>Sets whether to enable binary vacancy filling.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,1]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>BM_LOCAL_BLOCK
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">ThresholdCompensation<br>(Optional)</td>
        <td><b>Description</b><br>Constant subtracted from the mean or weighted mean used for calculating the threshold. Normally, it is positive but may be zero or negative as well.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[-255, 255]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>BM_LOCAL_BLOCK
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">BinarizationThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the binarization threshold.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[-1, 255]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>BM_THRESHOLD
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top"><br>MorphOperation(Optional)</td>
        <td><b>Description</b><br>Sets the morph operation for the morphology process.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>"Erode", "Dilate", "Open", "Close", "Auto" or "None"
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">MorphOperationKernelSizeX<br>(Optional)</td>
        <td><b>Description</b><br>Sets the horizontal kernel size for the morphology process. 0 stands for auto.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 1000]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">MorphOperationKernelSizeY<br>(Optional)</td>
        <td><b>Description</b><br>Sets the vertical kernel size for the morphology process. 0 stands for auto.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 1000]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">MorphShape<br>(Optional)</td>
        <td><b>Description</b><br>Sets the morph shape for the morphology process.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>"Rectangle", "Cross" or "Ellipse"
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">GrayscaleEnhancementModesIndex<br>(Optional)</td>
        <td><b>Description</b><br>The index of a specific image preprocessing mode in the GrayscaleEnhancementModes parameter which the current binarization mode is applied to.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[-1, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LibraryFileName<br>(Optional)</td>
        <td><b>Description</b><br>Sets the file name of the library to load dynamically.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing file name.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LibraryParameters<br>(Optional)</td>
        <td><b>Description</b><br>The library must be in the same place with Dynamsoft Barcode Reader Library.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing parameters.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes.
        </td>
    </tr>
</table>

### Default Setting

If the `BinarizationModes` is not configured in your template file, the following settings will be used as the default settings.

#### For Stage SST_BINARIZE_IMAGE

```json
{
    "BinarizationModes" : 
    [
        {
            "BinarizationThreshold" : -1,
            "BlockSizeX" : 0,
            "BlockSizeY" : 0,
            "EnableFillBinaryVacancy" : 1,
            "GrayscaleEnhancementModesIndex" : -1,
            "Mode" : "BM_LOCAL_BLOCK",
            "MorphOperation" : "None",
            "MorphOperationKernelSizeX" : 0,
            "MorphOperationKernelSizeY" : 0,
            "MorphShape" : "Rectangle",
            "ThresholdCompensation" : 10
        }
    ]
}
```

#### For Stage SST_BINARIZE_TEXTURE_REMOVED_GRAYSCALE

```json
{
    "BinarizationModes" : 
    [
        {
            "BinarizationThreshold" : -1,
            "BlockSizeX" : 0,
            "BlockSizeY" : 0,
            "EnableFillBinaryVacancy" : 1,
            "GrayscaleEnhancementModesIndex" : -1,
            "Mode" : "BM_AUTO",
            "MorphOperation" : "None",
            "MorphOperationKernelSizeX" : 0,
            "MorphOperationKernelSizeY" : 0,
            "MorphShape" : "Rectangle",
            "ThresholdCompensation" : 10
        }
    ]
}
```

#### For DeformationResistingModes

```json
{
    "BinarizationMode" : 
    {
        "BinarizationThreshold" : -1,
        "BlockSizeX" : 0,
        "BlockSizeY" : 0,
        "EnableFillBinaryVacancy" : 1,
        "GrayscaleEnhancementModesIndex" : -1,
        "Mode" : "BM_LOCAL_BLOCK",
        "MorphOperation" : "None",
        "MorphOperationKernelSizeX" : 0,
        "MorphOperationKernelSizeY" : 0,
        "MorphShape" : "Rectangle",
        "ThresholdCompensation" : 10
    }
}
```

## Candidate Modes Introduction

### BM_LOCAL_BLOCK

If an image has different lighting conditions in different areas, BM_LOCAL_BLOCK can help. In this case, our algorithm determines the threshold for a pixel based on a small region around it, which makes it more adaptive and gives better results.

**Available Mode Arguments:**

* BlockSizeX
* BlockSizeY
* EnableFillBinaryVacancy
* ThresholdCompensation
* BinarizationThreshold
* GrayscaleEnhancementModesIndex
* MorphOperation
* MorphShape
* MorphOperationKernelSizeX
* MorphOperationKernelSizeY
* LibraryFileName
* LibraryParameters

### BM_THRESHOLD

Binarizes the image for each pixel based on a unified threshold. If the gray value of the pixel is less than the threshold, it will be black in the binary image, otherwise it will be white.

**Available Mode Arguments:**

* BinarizationThreshold
* GrayscaleEnhancementModesIndex
* MorphOperation
* MorphShape
* MorphOperationKernelSizeX
* MorphOperationKernelSizeY
* LibraryFileName
* LibraryParameters
