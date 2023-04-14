---
layout: default-layout
title: ScaleUpModes - Dynamsoft Capture Vision Parameters
description: The parameter ScaleUpModes of Dynamsoft Capture Vision is for controlling the scale-up process when targets are too small in the image.
keywords: ScaleUpModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/scale-up-modes.html
---


# ScaleUpModes

ScaleUpModes is for controlling the scale-up process when targets in the image are too small.

**JSON Parameter Example**
```json
{
    "ScaleUpModes": [
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
Parameter ScaleUpModes consists of one or more of the following modes, each mode representing a different scale up algorithm:

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
            <li>SUM_LINEAR_INTERPOLATION</li>
            <li>SUM_NEAREST_NEIGHBOUR_INTERPOLATION</li>
            <li>SUM_AUTO</li>
            <li>SUM_SKIP</li>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        <li>SUM_AUTO</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">AcuteAngleWithXThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the acute angle threshold for barcode scale-up.
        <li>-1: means automatically set by the library.</li>
        <li>If the module size of the barcode is smaller than the ModuleSizeThreshold and the acute angle with X of the barcode is larger than the AcuteAngleWithXThreshold, the barcode will be enlarged by a scale factor of N (the value of N is a power of 2) till N * modulesize >= TargetModuleSize.</li>
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
        <li>SUM_LINEAR_INTERPOLATION</li>
        <li>SUM_NEAREST_NEIGHBOUR_INTERPOLATION</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ModuleSizeThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the module size threshold for barcode scale-up.
        <li>0: means automatically set by the library.</li>
        <li>If the module size of the barcode is smaller than the ModuleSizeThreshold and the acute angle with X of the barcode is larger than the AcuteAngleWithXThreshold, the barcode will be enlarged by a scale factor of N (the value of N is a power of 2) till N * modulesize >= TargetModuleSize.</li>
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
        <li>SUM_LINEAR_INTERPOLATION</li>
        <li>SUM_NEAREST_NEIGHBOUR_INTERPOLATION</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">TargetModuleSize<br>(Optional)</td>
        <td><b>Description</b><br>Sets the module size threshold for barcode scale-up.
        <li>0: means automatically set by the library.</li>
        <li>If the module size of the barcode is smaller than the ModuleSizeThreshold and the acute angle with X of the barcode is larger than the AcuteAngleWithXThreshold, the barcode will be enlarged by a scale factor of N (the value of N is a power of 2) till N * modulesize >= TargetModuleSize.</li>
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
        <li>SUM_LINEAR_INTERPOLATION</li>
        <li>SUM_NEAREST_NEIGHBOUR_INTERPOLATION</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LetterHeightThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the letter height threshold for character scale-up.
        <li>0 : means automatically set by the library. If the average letter height of a text line is smaller than the LetterHeightThreshold, the image will be enlarged to N times (N=2,4,8…) till N * LetterHeight >= TargetLetterHeight.</li>
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
        <li>SUM_LINEAR_INTERPOLATION</li>
        <li>SUM_NEAREST_NEIGHBOUR_INTERPOLATION</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">TargetLetterHeight<br>(Optional)</td>
        <td><b>Description</b><br>Sets the target letter height for character scale-up.
        <li>0 : means automatically set by the library.</li>
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
        <li>SUM_LINEAR_INTERPOLATION</li>
        <li>SUM_NEAREST_NEIGHBOUR_INTERPOLATION</li>
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

The default settings of ScaleUpModes is:

```json
{
    "ScaleUpModes" : [
         {
            "Mode" : "SUM_AUTO"
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



## See Also
- [Capture Vision Template]()
- [Image Parameter]() 