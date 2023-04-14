---
layout: default-layout
title: RegionPredetectionModes - Dynamsoft Capture Vision Parameters
description: The parameter RegionPredetectionModes of Dynamsoft Capture Vision is for detecting the region of interest(s) automatically.
keywords: RegionPredetectionModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/region-predetection-modes.html
---


# RegionPredetectionModes

RegionPredetectionModes controls how to find a region of interest (ROI) within the image or frame.

**JSON Parameter Example**
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
            "ForeAndBackgroundColours":[20,170,10],
            "WidthRange": "[100, 200]"
        }
    ]
}
```

## Parameter Summary
Parameter RegionPredetectionModes consists of one or more of the following modes, each mode representing a different detection algorithm:

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Any one in Candidate Mode List as string
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>
            <li>RPM_SKIP</li>
            <li>RPM_AUTO</li>
            <li>RPM_GENERAL</li>
            <li>RPM_GENERAL_RGB_CONTRAST</li>
            <li>RPM_GENERAL_GRAY_CONTRAST</li>
            <li>RPM_GENERAL_HSV_CONTRAST</li>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>RPM_GENERAL
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">AspectRatioRange<br>(Optional)</td>
        <td><b>Description</b><br>Specifies a set (or multiple sets) of aspect ratio range for filtering the predetected region:
        <li>A set of aspect ratio range is defined as [MinAspectRatio, MaxAspectRatio].
        <li>Using a "";"" to separate multiple sets.</li>
        <li>Value range of MinAspectRatio, MaxAspectRatio: [1,10000].</li>
        <li>Aspect ratio equals to height/width*100, while the height and width is from the bounding rectangle of the predetected region.</li>
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing aspect ratio range sets.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>RPM_GENERAL_HSV_CONTRAST</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">FindAccurateBoundary<br>(Optional)</td>
        <td><b>Description</b><br>Sets whether to enable finding accurate boundary:
        <li>0: disable.</li>
        <li>1: enable.</li>
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
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>RPM_GENERAL_HSV_CONTRAST</li>
            <li>RPM_GENERAL_RGB_CONTRAST</li>
            <li>RPM_GENERAL_GRAY_CONTRAST</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ForeAndBackgroundColours<br>(Optional)</td>
        <td><b>Description</b><br>Specifies a set (or multiple sets) of the foreground and background colours used for region predetection algorithm based on HSV colour space:
        <li>This argument is mandatory for RPM_GENERAL_HSV_CONTRAST mode. If there is no manual setting, no region can be detected.</li>
        <li>A set of the foreground and background colours is defined as [ForegroundColour, BackgroundColour, Tolerance].</li>
        <li>Using a "";"" to separate multiple sets.</li>
        <li>ForegroundColourand BackgroundColour are the Hue values in the HSV colour space for defining the foreground and background colours of the regions you want to predetect. The value -1 means black, gray, white.</li>
        <li>Tolerance is the allowable deviation of the Hue value defined by ForegroundColour.</li>
        <li>Value range of ForegroundColour, BackgroundColour: [-1,360].</li>
        <li>Value range of Tolerance: [0, 360].</li>
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing one or more colour sets.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>RPM_GENERAL_HSV_CONTRAST
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">HeightRange<br>(Optional)</td>
        <td><b>Description</b><br>Specifies a set (or multiple sets) of height range for filtering the predetected region:
        <li>A set of height is defined as [MinHeight, MaxHeight].</li>
        <li>Using a "";"" to separate multiple sets.</li>
        <li>Value range of MinHeight, MaxHeight: [1, 0x7fffffff].</li>
        <li>The height value is the height of the bounding rectangle of the predetected region.</li>
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing height range sets.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>RPM_GENERAL_HSV_CONTRAST</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">WidthRange<br>(Optional)</td>
        <td><b>Description</b><br>Specifies a set (or multiple sets) of width range for filtering the predetected region:
        <li>A set of width is defined as [MinWidth, MaxWidth].</li>
        <li>Using a "";"" to separate multiple sets.</li>
        <li>Value range of MinWidth, MaxWidth: [1, 0x7fffffff].</li>
        <li>The width value is the width of the bounding rectangle of the predetected region.</li>
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing height range sets.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>RPM_GENERAL_HSV_CONTRAST</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">MinImageDimension<br>(Optional)</td>
        <td><b>Description</b><br>Sets the minimum image dimension (in pixels) to enable region pre-detection:
        <li>The library will enable the region pre-detection feature only when the image dimension is larger than the given value.</li>
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
        <td><b>Default Value</b><br>262144
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>RPM_GENERAL_HSV_CONTRAST</li>
            <li>RPM_GENERAL_RGB_CONTRAST</li>
            <li>RPM_GENERAL_GRAY_CONTRAST</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">RelativeBarcodeRegions<br>(Optional)</td>
        <td><b>Description</b><br>Sets the barcode regions relative to the pre-detected region:
        <li>Each region need to be defined as [Left, Top, Right, Bottom, Index]. If you want to define multiple regions, you can use a "";"" to separate them. If there is no region defined, the library will consider the predetected regions as barcode regions.</li>
        <li>Left, Top, Right, Bottom are four percentage values relative to top-left corner of the predetected region.</li>
        <li>Index means the index of a specific colour set in ForeAndBackgroundColours which the current region is applied to. If the value of index is set to -1, the current region will be applied to all colour sets in ForeAndBackgroundColours.</li>
        <li>Value range of Left, Top, Right, Bottom: [-10000,10000].</li>
        <li>Value range of Index: [-1, 0x7fffffff].</li>
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing one or more regions.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>RPM_GENERAL_HSV_CONTRAST</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Sensitivity<br>(Optional)</td>
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
        <td><b>Default Value</b><br>1
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>RPM_GENERAL_HSV_CONTRAST</li>
            <li>RPM_GENERAL_RGB_CONTRAST</li>
            <li>RPM_GENERAL_GRAY_CONTRAST</li>
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
            <li>RPM_GENERAL_HSV_CONTRAST</li>
            <li>RPM_GENERAL_RGB_CONTRAST</li>
            <li>RPM_GENERAL_GRAY_CONTRAST</li>
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
        <td><b>Valid For</b><br>All modes.
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

The default settings of RegionPredetectionModes is:

```json
{
    "RegionPredetectionModes": [
         {
            "Mode" : "RPM_GENERAL"
         }
      ]
}
```


## Candidate Modes Introduction

### RPM_SKIP
Skip region pre-detection process.

### RPM_AUTO
Lets the library choose a mode automatically.

### RPM_GENERAL
Takes the whole image as a region. This mode has the following arguments for further customizing.
**Available auxiliary parameters:**
- [LibraryFileName]()
- [LibraryParameters]()

### RPM_GENERAL_RGB_CONTRAST
Detects region using the general algorithm based on RGB colour contrast. This mode has the following arguments for further customizing.
**Available auxiliary parameters:**
- [MinImageDimension]()
- [Sensitivity]()
- [SpatialIndexBlockSize]()
- [LibraryFileName]()
- [LibraryParameters]()

### RPM_GENERAL_GRAY_CONTRAST
Detects region using the general algorithm based on gray contrast. This mode has the following arguments for further customizing.
**Available auxiliary parameters:**
- [MinImageDimension]()
- [Sensitivity]()
- [SpatialIndexBlockSize]()
- [LibraryFileName]()
- [LibraryParameters]()

### RPM_GENERAL_HSV_CONTRAST
Detects region using the general algorithm based on HSV colour contrast. This mode has the following arguments for further customizing.
**Available auxiliary parameters:**
- [AspectRatioRange]()
- [FindAccurateBoundary]()
- [ForeAndBackgroundColours]()
- [HeightRange]()
- [WidthRange]()
- [RelativeBarcodeRegions]()
- [MinImageDimension]()
- [Sensitivity]()
- [SpatialIndexBlockSize]()
- [LibraryFileName]()
- [LibraryParameters]()

## See Also
- [Capture Vision Template]()
- [Image Parameter]() 