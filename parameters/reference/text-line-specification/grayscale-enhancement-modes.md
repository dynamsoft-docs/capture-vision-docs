---
layout: default-layout
title: GrayscaleEnhancementModes - Dynamsoft Label Recognizer Parameters
description: The parameter GrayscaleEnhancementModes of text line specification is for enhancing the quality of grayscale image of the text line area.
keywords: GrayscaleEnhancementModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---


# GrayscaleEnhancementModes

Parameter `GrayscaleEnhancementModes` provides some image processing methods to enhance the grayscale quality of the text line area. By default, the library does no image preprocessing. Assume your image has distorted features that can be solved by common image processing methods, this parameter can help you get a higher quality grayscale image by shifting the order of the preprocessing algorithms used (if at all).

## Example

```json
{
    "GrayscaleEnhancementModes": [
        {
            "Mode": "GEM_GRAY_EQUALIZE", 
            "Sensitivity": 1
        },
        {
            "Mode": "GEM_GRAY_SMOOTH", 
            "SmoothBlockSizeX": 5,
            "SmoothBlockSizeY": 5
        },
        {
            "Mode": "GEM_SHARPEN_SMOOTH", 
            "SmoothBlockSizeX": 5,
            "SmoothBlockSizeY": 5,
            "SharpenBlockSizeX": 5,
            "SharpenBlockSizeY": 5
        }
    ]
}
```

## Parameter Summary

Parameter `GrayscaleEnhancementModes` consist of a group of grayscale enhancement mode objects. Each grayscale enhancement mode object includes a candidate mode and a series of mode arguments. The mode arguments of the grayscale enhancement mode object is shown as follow:

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
        <td><b>Candidate Mode List</b><br>GEM_GENERAL
            <br>GEM_GRAY_EQUALIZE
            <br>GEM_GRAY_SMOOTH
            <br>GEM_SHARPEN_SMOOTH
            <br>GEM_SKIP
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>GEM_GENERAL
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Sensitivity<br>(Optional)</td>
        <td><b>Description</b><br>Sets the sensitivity to perform the equalization process. A larger value means a higher possibility that gray equalization will be activated.
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
        <td><b>Default Value</b><br>5
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>GEM_GRAY_EQUALIZE
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">SmoothBlockSizeX<br>(Optional)</td>
        <td><b>Description</b><br>Sets the horizontal block size(neighborhood pixel counts) for the smoothing process.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[3,1000]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>3
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>GEM_GRAY_SMOOTH
            <br>GEM_SHARPEN_SMOOTH
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">SmoothBlockSizeY<br>(Optional)</td>
        <td><b>Description</b><br>Sets the vertical block size(neighborhood pixel counts) for the smoothing process.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[3,1000]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>3
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>GEM_GRAY_SMOOTH
            <br>GEM_SHARPEN_SMOOTH
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">SharpenBlockSizeX<br>(Optional)</td>
        <td><b>Description</b><br>Sets the horizontal block size(neighborhood pixel counts) for the sharpening process.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[3,1000]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>3
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>GEM_SHARPEN_SMOOTH
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">SharpenBlockSizeY<br>(Optional)</td>
        <td><b>Description</b><br>Sets the vertical block size(neighborhood pixel counts) for the sharpening process.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[3,1000]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>3
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>GEM_SHARPEN_SMOOTH
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

If the `GrayscaleEnhancementModes` is not configured in your template file, the following settings will be used as the default settings.

```json
{
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
    ]
}
```

## Candidate Modes Introduction

### GEM_GENERAL

Takes the un-preprocessed grayscale image for the next stage of operations.

### GEM_GRAY_EQUALIZE

Preprocesses the grayscale image using the gray equalization algorithm. This mode can be used for images with low contrast between content and background colour.

**Available Mode Arguments:**

* Sensitivity

### GEM_GRAY_SMOOTH

Preprocesses the grayscale image using the gray smoothing algorithm. This mode can be used for for images with noise or texture.

**Available Mode Arguments:**

* SmoothBlockSizeX
* SmoothBlockSizeY

### GEM_SHARPEN_SMOOTH

Preprocesses the grayscale image using the sharpening and smoothing algorithm. This mode can be used for blurry images.

**Available Mode Arguments:**

* SmoothBlockSizeX
* SmoothBlockSizeY
* SharpenBlockSizeX
* SharpenBlockSizeY
