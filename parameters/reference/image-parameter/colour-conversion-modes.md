---
layout: default-layout
title: ColourConversionModes - Dynamsoft Capture Vision Parameters
description: The parameter ColourConversionModes of Dynamsoft Capture Vision is for controlling the converting of colour image to grayscale image.
keywords: ColourConversionModes, parameter reference, parameter
---


# ColourConversionModes

Parameter `ColourConversionModes` is a parameter for setting the mode for converting a colour image to a grayscale image. It consists of one or more `ColourConversionMode` items and each item has its own arguments.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_CONVERT_TO_GRAYSCALE")
        └── ColourConversionModes
```

**Parent object:** [ConvertToGrayscaleStage](stage-convert-to-grayscale.md)

**Example:**

```json
{
    "ColourConversionModes": [
        {
            "Mode": "CICM_GENERAL"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `ColourConversionModes` parameter.
> - To use it, embed this parameter within a [ConvertToGrayscaleStage](stage-convert-to-grayscale.md) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

Parameter `ColourConversionModes` consist of a group of colour conversion mode objects. Each colour conversion mode object includes a candidate mode and a series of mode arguments. The mode arguments of the colour conversion mode object is shown as follow:

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
        <td><b>Candidate Mode List</b><br>CICM_HSV
            <br>CICM_GENERAL
            <br>CICM_EDGE_ENHANCEMENT
            <br>CICM_SKIP
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
        <td><b>Valid For</b><br>CICM_GENERAL
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
        <td><b>Valid For</b><br>CICM_GENERAL
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
        <td><b>Valid For</b><br>CICM_GENERAL
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
        <td><b>Range</b><br>"H_CHANNEL","S_CHANNEL","V_CHANNEL"
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>"H_CHANNEL"
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>CICM_HSV
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

#### For Barcode Decoding & Label Recognizing

If the `ColourConversionModes` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "ColourConversionModes" : 
    [
        {
            "BlueChannelWeight" : -1,
            "GreenChannelWeight" : -1,
            "Mode" : "CICM_GENERAL",
            "RedChannelWeight" : -1,
            "ReferChannel" : "H_CHANNEL"
        }
    ]
}
```

#### For Document Detection

In document detection tasks, various ColuorConversionModes will be tried as much as possible to gather sufficient information for subsequent line detection and assembly.

```json
{
    "ColourConversionModes" : 
    [
        {
            "BlueChannelWeight" : -1,
            "GreenChannelWeight" : -1,
            "Mode" : "CICM_GENERAL",
            "RedChannelWeight" : -1,
        },
        {
            "Mode" : "CICM_EDGE_ENHANCEMENT"
        },
        {
            "Mode" : "CICM_HSV",
            "ReferChannel" : "H_CHANNEL"
        }
    ]
}
```

## Candidate Mode Introductions

### CICM_GENERAL

Converts a colour image to a grayscale image using the general RGB colour model.

**Available Mode Arguments:**

* RedChannelWeight
* BlueChannelWeight
* GreenChannelWeight
* LibraryFileName
* LibraryParameters

### CICM_EDGE_ENHANCEMENT

Converts a colour image to a grayscale image, and enhances the pixel value of points with more significant contrast, to highlight edge features during conversion.

**Available Mode Arguments:**

* LibraryFileName
* LibraryParameters

### CICM_HSV

Converts a colour image to a grayscale image using the HSV colour model.

**Available Mode Arguments:**

* ReferChannel
* LibraryFileName
* LibraryParameters
