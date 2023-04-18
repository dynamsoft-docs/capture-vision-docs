---
layout: default-layout
title: GrayscaleEnhancementModes - Dynamsoft Capture Vision Parameters
description: The parameter GrayscaleEnhancementModes of Dynamsoft Capture Vision is for enhancing the quality of grayscale image.
keywords: GrayscaleEnhancementModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/grayscale-enhancement-modes.html
---


# GrayscaleEnhancementModes

GrayscaleEnhancementModes provides some image processing methods to enhance the quality of the grayscale image. By default, the library does no image preprocessing. Assume your image has distorted features that can be solved by common image processing methods, this parameter can help you get a higher quality grayscale image by shifting the order of the preprocessing algorithms used (if at all).

**JSON Parameter Example**   
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
Parameter GrayscaleEnhancementModes consists of one or more of the following modes, each mode representing a different preprocessing algorithm:

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
            <li>GEM_GENERAL</li>
            <li>GEM_GRAY_EQUALIZE</li>
            <li>GEM_GRAY_SMOOTH</li>
            <li>GEM_SHARPEN_SMOOTH</li>
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
        <td><b>Valid For</b><br>
            <li>GEM_GRAY_EQUALIZE</li>
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
        <td><b>Valid For</b><br>
            <li>GEM_GRAY_SMOOTH</li>
            <li>GEM_SHARPEN_SMOOTH</li>
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
        <td><b>Valid For</b><br>
            <li>GEM_GRAY_SMOOTH</li>
            <li>GEM_SHARPEN_SMOOTH</li>
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
        <td><b>Valid For</b><br>
            <li>GEM_SHARPEN_SMOOTH</li>
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
        <td><b>Valid For</b><br>
            <li>GEM_SHARPEN_SMOOTH</li>
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

The default settings of GrayscaleEnhancementModes is:

```json
{
    "GrayscaleEnhancementModes": [
        {
            "Mode": "GEM_GENERAL" 
        }
    ]
}
```


## Candidate Modes Introduction

### GEM_GENERAL

Takes the un-preprocessed grayscale image for the next stage of operations.


### GEM_GRAY_EQUALIZE

Preprocesses the grayscale image using the gray equalization algorithm. This mode can be used for images with low contrast between content and background colour.

**Available auxiliary parameters:**

- [Sensitivity]()

### GEM_GRAY_SMOOTH

Preprocesses the grayscale image using the gray smoothing algorithm. This mode can be used for for images with noise or texture.

**Available auxiliary parameters:**

- [SmoothBlockSizeX]()
- [SmoothBlockSizeY]()

### GEM_SHARPEN_SMOOTH

Preprocesses the grayscale image using the sharpening and smoothing algorithm. This mode can be used for blurry images.

**Available auxiliary parameters:**

- [SmoothBlockSizeX]()
- [SmoothBlockSizeY]()
- [SharpenBlockSizeX]()
- [SharpenBlockSizeY]()

## See Also
- [Capture Vision Template]()
- [Image Parameter]() 