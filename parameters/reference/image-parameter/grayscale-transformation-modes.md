---
layout: default-layout
title: GrayscaleTransformationModes - Dynamsoft Capture Vision Parameters
description: The parameter GrayscaleTransformationModes of Dynamsoft Capture Vision is for controlling the inversion of colors in grayscale image.
keywords: GrayscaleTransformationModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/gray-scale-transformation-modes.html
---


# GrayscaleTransformationModes

Generally, we think of the lighter colors as the background and the darker colors as the target in a grayscale image. However in a few cases it is opposite. GrayscaleTransformationModes are used to control whether or not to invert the color of the grayscale image.

**JSON Parameter Example**   
```json
{
    "GrayscaleTransformationModes": [
        {
            "Mode": "GTM_ORIGINAL"
        },
        {
            "Mode": "GTM_INVERTED" 
        }
    ]
}
```

## Parameter Summary
Parameter GrayscaleTransformationModes consists of one or more of the following modes, each mode representing a different preprocessing algorithm:

<table style = "text-align:left">
    <tr>
        <th>GrayscaleTransformationModes Parameter Details</th>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>
            <li>GTM_ORIGINAL</li>
            <li>GTM_INVERTED</li>
            <li>GTM_AUTO</li>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>GTM_ORIGINAL
        </td>
    </tr>
    
</table>

The default settings of GrayscaleTransformationModes is:

```json
{
    "GrayscaleTransformationModes": [
        {
            "Mode": "GTM_ORIGINAL" 
        }
    ]
}
```


## Candidate Modes Introduction

### GTM_ORIGINAL

Keeps the original grayscale.

### GTM_INVERTED

Transforms the image to inverted grayscale.

### GTM_INVERTED

Let the library choose automatically for grayscale transformation.

## See Also
- [Capture Vision Template]()
- [Image Parameter]() 