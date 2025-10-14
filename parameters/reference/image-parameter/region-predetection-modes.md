---
layout: default-layout
title: RegionPredetectionModes * Dynamsoft Capture Vision Parameters
description: The parameter RegionPredetectionModes of Dynamsoft Capture Vision is for detecting the region of interest(s) automatically.
keywords: RegionPredetectionModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---


# RegionPredetectionModes

Parameter `RegionPredetectionModes` controls how to find a region of interest (ROI) within the image or frame.

```json
{
    "RegionPredetectionModes": [
        {
            "Mode": "RPM_GENERAL_GRAY_CONTRAST", 
            "Sensitivity": 5
        },
        {
            "Mode": "RPM_GENERAL_RGB_CONTRAST", 
            "Sensitivity": 5
        },
        {
            "Mode": "RPM_GENERAL_HSV_CONTRAST", 
            "ForeAndBackgroundColours":"[20,170,10]",
            "WidthRange": "[100, 200]"
        },
        {
            "Mode": "RPM_NEURAL_NETWORK",
            "DetectionModelName": ""
        }        
    ]
}
```

## Parameter Summary

### Mode Arguments

Parameter `RegionPredetectionModes` consist of a group of region predetection mode objects. Each region predetection  mode object includes a candidate mode and a series of mode arguments. The mode arguments of the region predetection mode object is shown as follow:

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
        <td><b>Candidate Mode List</b><br>
            RPM_SKIP<br>
            RPM_AUTO<br>
            RPM_GENERAL<br>
            RPM_GENERAL_RGB_CONTRAST<br>
            RPM_GENERAL_GRAY_CONTRAST<br>
            RPM_GENERAL_HSV_CONTRAST<br>
            RPM_GRAY_CONSISTENCY
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">AspectRatioRange<br>(Optional)</td>
        <td><b>Description</b><br>Specifies one or multiple sets of aspect ratio ranges as a string for filtering the predetected region.<br><br><i>Aspect Ratio = BoundingRectHeight/BoundingRectWidth * 100</i>
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Substruct</b><br>Define one range:<br>"[MinAspectRatio, MaxAspectRatio]"<br>Define multiple ranges:<br>"[MinAspectRatio, MaxAspectRatio];[MinAspectRatio, MaxAspectRatio];..."
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>MinAspectRatio: [0,10000]<br>MaxAspectRatio: [0,10000]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            RPM_GENERAL_HSV_CONTRAST<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">FindAccurateBoundary<br>(Optional)</td>
        <td><b>Description</b><br>Sets whether to enable finding accurate boundary:<br>
        0: disable.<br>
        1: enable.
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
        <td><b>Valid For</b><br>
            RPM_GENERAL_HSV_CONTRAST<br>
            RPM_GENERAL_RGB_CONTRAST<br>
            RPM_GENERAL_GRAY_CONTRAST
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ForeAndBackgroundColours<br>(Required by RPM_GENERAL_HSV_CONTRAST )</td>
        <td><b>Description</b><br>Specifies a set (or multiple sets) of the foreground and background colours used for region predetection algorithm based on HSV colour space:<br>
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Substruct</b><br>Define one range:<br>"[ForegroundColour,BackgroundColour,Tolerance]"<br>Define multiple ranges:<br>"[ForegroundColour,BackgroundColour,Tolerance];[ForegroundColour,BackgroundColour,Tolerance];..."
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>ForegroundColour: [-1,360]<br>BackgroundColour: [-1,360]<br>Tolerance: [0, 360]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>RPM_GENERAL_HSV_CONTRAST
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">HeightRange<br>(Optional)</td>
        <td><b>Description</b><br>Specifies a set (or multiple sets) of height range for filtering the predetected region. The height is measured by the height of the bounding rect of the predetected region.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Substruct</b><br>Define one range:<br>"[MinHeight, MaxHeight]"<br>Define multiple ranges:<br>"[MinHeight, MaxHeight];[MinHeight, MaxHeight];..."
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>MinHeight: [1, 0x7fffffff]<br>MaxHeight: [1, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            RPM_GENERAL_HSV_CONTRAST<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">WidthRange<br>(Optional)</td>
        <td><b>Description</b><br>Specifies a set (or multiple sets) of width range for filtering the predetected region. The width is measured by the width of the bounding rect of the predetected region.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Substruct</b><br>Define one range:<br>"[MinWidth, MaxWidth]"<br>Define multiple ranges:<br>"[MinWidth, MaxWidth];[MinWidth, MaxWidth];..."
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing height range sets.
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            RPM_GENERAL_HSV_CONTRAST<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">MinImageDimension<br>(Optional)</td>
        <td><b>Description</b><br>Sets the minimum image dimension (in pixels) to enable region pre-detection.
        The library will enable the region pre-detection feature only when the image dimension is larger than the given value.<br>
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[16384, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            RPM_GENERAL_HSV_CONTRAST<br>
            RPM_GENERAL_RGB_CONTRAST<br>
            RPM_GENERAL_GRAY_CONTRAST<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "6" style="vertical-align:text-top">RelativeRegions<br>(Optional)</td>
        <td><b>Description</b><br>Sets the barcode regions relative to the pre-detected region.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Substruct</b><br>Define one region:<br>"[Left,Top,Right,Bottom,Index]"<br>Define multiple region:<br>"[Left,Top,Right,Bottom,Index];[Left,Top,Right,Bottom,Index];..."
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>Left, Top, Right, Bottom: [-10000,10000]<br>Index: [-1,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            RPM_GENERAL_HSV_CONTRAST<br>
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Parameters Left, Top, Right, Bottom are measured in percentage.<br>Parameter Index points to a specific colour that set in ForeAndBackgroundColours. Set it to -1 to apply the current RelativeRegion to all ForeAndBackgroundColours.
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Sensitivity<br>(Optional)</td>
        <td><b>Description</b><br>Sets the sensitivity used for region predetection algorithm, a larger value means the library will take more effort to detect regions.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[1,9]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            RPM_GENERAL_HSV_CONTRAST<br>
            RPM_GENERAL_RGB_CONTRAST<br>
            RPM_GENERAL_GRAY_CONTRAST<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">SpatialIndexBlockSize<br>(Optional)</td>
        <td><b>Description</b><br>Sets the spatial index block size used for region predetection algorithm. The block size used for region predetection would be 2 to the power of N. The allowed values of SpatialIndexBlockSize is the power number (N=1,2,3…).
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[1, 32]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>5
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            RPM_GENERAL_HSV_CONTRAST<br>
            RPM_GENERAL_RGB_CONTRAST<br>
            RPM_GENERAL_GRAY_CONTRAST<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">GrayRange<br>(Optional)</td>
        <td><b>Description</b><br>Sets the target grayscale value range, formatted as [MinGrayValue, MaxGrayValue], for candidate regions.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>Int Array</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>MinGrayValue: [0,255]<br>MaxGrayValue: [0,255]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>[0,255]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>RPM_GRAY_CONSISTENCY.
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">MatchRatio<br>(Optional)</td>
        <td><b>Description</b><br>Sets the minimum percentage of pixels within a spatial block that must fall into the `GrayRange` for the block to be considered consistent.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>Int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 100]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>50
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>RPM_GRAY_CONSISTENCY
        </td>
    </tr>
</table>

### Default Setting

The default settings of RegionPredetectionModes is:

```json
{
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
}
```

## Candidate Modes Introduction

### RPM_SKIP

Skip region pre-detection process.

### RPM_AUTO

Lets the library choose a mode automatically.

### RPM_GENERAL

Takes the whole image as a region. This mode has the following arguments for further customizing.

### RPM_GENERAL_RGB_CONTRAST

Detects region using the general algorithm based on RGB colour contrast. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

* MinImageDimension
* Sensitivity
* SpatialIndexBlockSize

### RPM_GENERAL_GRAY_CONTRAST

Detects region using the general algorithm based on gray contrast. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

* MinImageDimension
* Sensitivity
* SpatialIndexBlockSize

### RPM_GENERAL_HSV_CONTRAST

Detects region using the general algorithm based on HSV colour contrast. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

* AspectRatioRange
* FindAccurateBoundary
* ForeAndBackgroundColours
* HeightRange
* WidthRange
* RelativeBarcodeRegions
* MinImageDimension
* Sensitivity
* SpatialIndexBlockSize

### RPM_GRAY_CONSISTENCY

Detects regions in a grayscale image where pixel values fall within a specified gray range and demonstrate local consistency. This is useful for locating areas with uniform brightness, such as document backgrounds or label zones.

**Available Mode Arguments:**

* GrayRange
* MatchRatio

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.
