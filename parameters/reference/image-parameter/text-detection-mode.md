---
layout: default-layout
title: TextDetectionMode - Dynamsoft Capture Vision Parameters
description: The parameter TextDetectionMode of Dynamsoft Capture Vision is for detecting texts on an image.
keywords: TextDetectionMode, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /parameters/reference/image-parameter/text-detection-mode.html
---


# TextDetectionMode

Parameter `TextDetectionMode` determines how to detect the text area. For tasks like barcode reading or border detection, the text part is not important; while for the task of text recognition, the results of detected text zone are mandatory.

## Example

```json
{
    "TextDetectionMode":
    {
        "Mode": "TTDM_WORD",
        "Direction": "HORIZONTAL",
        "CharHeightRange": [1,1000,1]
    }
}
```

## Parameter Summary

Parameter `TextDetectionMode` consist of a group of text detection mode objects. Each text detection mode object includes a candidate mode and a series of mode arguments. The mode arguments of the text detection mode object is shown as follow:

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
        <td><b>Candidate Mode List</b><br>TTDM_WORD
            <br>TTDM_LINE
            <br>TTDM_LAYOUT
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Direction<br>(Optional)</td>
        <td><b>Description</b><br>Set the direction to perform text zone detection.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>"HORIZONTAL", "VERTICAL", "OBLIQUE"
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>"HORIZONTAL"
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">CharHeightRange<br>(Optional)</td>
        <td><b>Description</b><br>Sets the range of letter height in pixel or a percentage.
        <br>Format: [MinHeight, MaxHeight, ByThousandth].
        <br>if ByThousandth=1, the allowed values for MinHeight/MaxHeight=[1, 1000]
        <br>if ByThousandth=0, the allowed values for MinHeight/MaxHeight=[1, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int array</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[1, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>[1,1000,1]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">MaxSpacingInALine<br>(Optional)</td>
        <td><b>Description</b><br>Sets the maximum spacing between characters treated as one line.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[-1, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>-1
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>TTDM_LINE
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>0: means automatically set by the library.<br>It is a percentage value relative to the average letter height of each line.<br>All TextArea Objects without MaxLineCharacterSpacing set will be set from this setting.
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

#### For Barcode Decoding

```json
{
    "TextDetectionMode" : 
    {
        "CharHeightRange" : 
        [
            1,
            1000,
            1
        ],
        "Direction" : "HORIZONTAL",
        "MaxSpacingInALine" : -1,
        "Mode" : "TTDM_SKIP"
    }   
}
```

#### For Label Recognizing

```json
{
    "TextDetectionMode" : 
    {
        "CharHeightRange" : 
        [
            1,
            1000,
            1
        ],
        "Direction" : "HORIZONTAL",
        "MaxSpacingInALine" : -1,
        "Mode" : "TTDM_LINE"
    }
}
```

#### For Document Scanning

```json
{
    "TextDetectionMode" : 
    {
        "CharHeightRange" : 
        [
            1,
            1000,
            1
        ],
        "Direction" : "HORIZONTAL",
        "MaxSpacingInALine" : -1,
        "Mode" : "TTDM_WORD"
    }
}
```

## Candidate Modes Introduction

### TTDM_WORD

Find the text area based on the "word" objects. It is the fastest text detection mode but has the lowest accuracy.

### TTDM_LINE

Find the text area based on the "text line" objects. This mode has higher accuracy than the `TTDM_WORD`. It is currently implemented as the default mode for text line recognizing.

### TTDM_LAYOUT

Find the text area based on the layout. A mode with even higher accuracy than the `TTDM_LINE`. Not supported yet.
