---
layout: default-layout
title: ColourConversionModes - Dynamsoft Capture Vision Parameters
description: The parameter ColourConversionModes of Dynamsoft Capture Vision is for controlling the converting of colour image to grayscale image.
keywords: ColourConversionModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/colour-conversion-modes.html
---


# ColourConversionModes

ColourConversionModes is a parameter for setting the mode for converting a colour image to a grayscale image. It consists of one or more ColourConversionMode items and each item has its own arguments.

**JSON Parameter Example**   
```json
{
    "ColourConversionModes": [
        {
            "Mode": "CICM_GENERAL"
        }
    ]
}
```


## Parameter Summary
Parameter ColourConversionModes consist of a group of colour conversion mode objects. Each colour conversion mode object includes a candidate mode and a series of auxiliary parameters. The structure of the localization mode object is shown as follow:

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
            <li>CICM_HSV</li>
            <li>CICM_GENERAL</li>
            <li>CICM_SKIP</li>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>CICM_GENERAL
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">BlueChannelWeight<br>(Optional)</td>
        <td><b>Description</b><br>Sets the weight value of Blue Colour Channel used for converting a colour image to a grayscale image.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[-1,1000]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>-1
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>CICM_GENERAL</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">GreenChannelWeight<br>(Optional)</td>
        <td><b>Description</b><br>Sets the weight value of Green Colour Channel used for converting a colour image to a grayscale image.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[-1,1000]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>-1
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>CICM_GENERAL</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">RedChannelWeight<br>(Optional)</td>
        <td><b>Description</b><br>Sets the weight value of Red Colour Channel used for converting a colour image to a grayscale image.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[-1,1000]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>-1
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>CICM_GENERAL</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ReferChannel<br>(Optional)</td>
        <td><b>Description</b><br>Sets reference channel used for converting a colour image to a grayscale image by HSV algorithm.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>string</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>“H_CHANNEL”,“S_CHANNEL”,“V_CHANNEL”
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>“H_CHANNEL”
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>CICM_HSV</li>
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

The default settings of ColourConversionModes is:

```json
"BinarizationModes" : [
         {
            "Mode" : "CICM_GENERAL",
            "RedChannelWeight" : -1,
            "BlueChannelWeight" : -1,
            "GreenChannelWeight" : -1,
            "LibraryFileName" : "",
            "LibraryParameters" : ""
         }
      ]
```


<!--
“CICM_SKIP”
“CICM_GENERAL”
“CICM_HSV”
-->



## Candidate Modes Introduction

### CICM_GENERAL

Converts a colour image to a grayscale image using the general RGB colour model.

**Available auxiliary parameters:**

- [RedChannelWeight]()
- [BlueChannelWeight]()
- [GreenChannelWeight]()
- [LibraryFileName](#libraryfilename)
- [LibraryParameters](#libraryparameters)

### CICM_HSV

Converts a colour image to a grayscale image using the HSV colour model.

**Available auxiliary parameters:**

- [ReferChannel]()
- [LibraryFileName](#libraryfilename)
- [LibraryParameters](#libraryparameters)

## See Also
- [Capture Vision Template]()
- [Image Parameter]() 