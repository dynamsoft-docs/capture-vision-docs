---
layout: default-layout
title: GrayscaleTransformationModes - Dynamsoft Capture Vision Parameters
description: The parameter GrayscaleTransformationModes of Dynamsoft Capture Vision is for controlling the inversion of colors in grayscale image.
keywords: GrayscaleTransformationModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /parameters/reference/image-parameter/grayscale-transformation-modes.html
---


# GrayscaleTransformationModes

Parameter `GrayscaleTransformationModes` are used to control whether or not to invert the color of the grayscale image. Generally, we think of the lighter colors as the background and the darker colors as the target in a grayscale image. However in a few cases it is opposite.

## Example

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

### Mode Arguments

Parameter `GrayscaleTransformationModes` consist of a group of grayscale transformation mode objects. Each grayscale transformation mode object includes a candidate mode and a series of mode arguments. The mode arguments of the grayscale transformation mode object is shown as follow:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Specifies a mode for grayscale transformation.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>GTM_ORIGINAL<br>GTM_INVERTED<br>GTM_AUTO
        </td>
    </tr>
</table>

### Default Setting

If the `GrayscaleTransformationModes` is not configured in your template file, the following settings will be used as the default settings.

#### For Barcode Decoding

```json
{
    "GrayscaleTransformationModes": 
    [
        {
            "Mode": "GTM_ORIGINAL" 
        }
    ]
}
```

#### For Label Recognizing

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


#### For Document Scanning

```json
{
    "GrayscaleTransformationModes": 
    [
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

### GTM_AUTO

Let the library choose automatically for grayscale transformation.