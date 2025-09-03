---
layout: default-layout
title: ScaleUpModes - Dynamsoft Capture Vision Parameters
description: The parameter ScaleUpModes of Dynamsoft Capture Vision is for controlling the scale-up process when targets are too small in the image.
keywords: ScaleUpModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /parameters/reference/image-parameter/scale-up-modes.html
---


# ScaleUpModes

Parameter `ScaleUpModes` is for controlling the scale-up process when targets in the image are too small.

## Example

```json
{
    "ScaleUpModes": 
    [
        {
            "Mode": "SUM_LINEAR_INTERPOLATION", 
            "ModuleSizeThreshold": 4,
            "TargetModuleSize": 8
        },
        {
            "Mode": "SUM_NEAREST_NEIGHBOUR_INTERPOLATION", 
            "ModuleSizeThreshold": 4,
            "TargetModuleSize": 6
        },
        {
            "Mode": "SUM_LINEAR_INTERPOLATION",
            "LetterHeightThreshold": 10,
            "TargetLetterHeight": 50
        }
    ]
}
```

## Parameter Summary

Parameter `ScaleUpModes` consist of a group of scale up mode objects. Each scale up mode object includes a candidate mode and a series of mode arguments. The mode arguments of the scale up mode object is shown as follow:

### Mode Arguments

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
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
        <td><b>Candidate Mode List</b><br>SUM_LINEAR_INTERPOLATION
            <br>SUM_NEAREST_NEIGHBOUR_INTERPOLATION
            <br>SUM_AUTO
            <br>SUM_SKIP
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        <br>SUM_AUTO
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">AcuteAngleWithXThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the acute angle threshold for barcode scale-up.
        <br>-1: means automatically set by the library.
        <br>If the module size of the barcode is smaller than the ModuleSizeThreshold and the acute angle with X of the barcode is larger than the AcuteAngleWithXThreshold, the barcode will be enlarged by a scale factor of N (the value of N is a power of 2) till N * modulesize >= TargetModuleSize.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[-1, 90]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>-1
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
        <br>SUM_LINEAR_INTERPOLATION
        <br>SUM_NEAREST_NEIGHBOUR_INTERPOLATION
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ModuleSizeThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the module size threshold for barcode scale-up.
        <br>0: means automatically set by the library.
        <br>If the module size of the barcode is smaller than the ModuleSizeThreshold and the acute angle with X of the barcode is larger than the AcuteAngleWithXThreshold, the barcode will be enlarged by a scale factor of N (the value of N is a power of 2) till N * modulesize >= TargetModuleSize.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[1, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
        <br>SUM_LINEAR_INTERPOLATION
        <br>SUM_NEAREST_NEIGHBOUR_INTERPOLATION
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">TargetModuleSize<br>(Optional)</td>
        <td><b>Description</b><br>Sets the module size threshold for barcode scale-up.
        <br>0: means automatically set by the library.
        <br>If the module size of the barcode is smaller than the ModuleSizeThreshold and the acute angle with X of the barcode is larger than the AcuteAngleWithXThreshold, the barcode will be enlarged by a scale factor of N (the value of N is a power of 2) till N * modulesize >= TargetModuleSize.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
        <br>SUM_LINEAR_INTERPOLATION
        <br>SUM_NEAREST_NEIGHBOUR_INTERPOLATION
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LetterHeightThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the letter height threshold for character scale-up.
        <br>0 : means automatically set by the library. If the average letter height of a text line is smaller than the LetterHeightThreshold, the image will be enlarged to N times (N=2,4,8…) till N * LetterHeight >= TargetLetterHeight.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
        <br>SUM_LINEAR_INTERPOLATION
        <br>SUM_NEAREST_NEIGHBOUR_INTERPOLATION
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">TargetLetterHeight<br>(Optional)</td>
        <td><b>Description</b><br>Sets the target letter height for character scale-up.
        <br>0 : means automatically set by the library.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
        <br>SUM_LINEAR_INTERPOLATION
        <br>SUM_NEAREST_NEIGHBOUR_INTERPOLATION
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

### Default Setting

If the `ScaleUpModes` is not configured in your template file, the following setting will be used as the default setting.

```json
{
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
    ]
}
```

## Candidate Modes Introduction

### SUM_LINEAR_INTERPOLATION

Scales up using the linear interpolation method. This mode has the following arguments for further customizing:

- AcuteAngleWithXThreshold
- ModuleSizeThreshold
- TargetModuleSize
- LetterHeightThreshold
- TargetLetterHeight
- LibraryFileName
- LibraryParameters

### SUM_NEAREST_NEIGHBOUR_INTERPOLATION

Scales up using the nearest neighbour method. This mode has the following arguments for further customizing:

- AcuteAngleWithXThreshold
- ModuleSizeThreshold
- TargetModuleSize
- LetterHeightThreshold
- TargetLetterHeight
- LibraryFileName
- LibraryParameters

### SUM_AUTO

Lets the library choose a mode automatically.
