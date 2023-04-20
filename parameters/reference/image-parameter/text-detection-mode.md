---
layout: default-layout
title: TextDetectionMode - Dynamsoft Capture Vision Parameters
description: The parameter TextDetectionMode of Dynamsoft Capture Vision is for detecting texts on an image.
keywords: TextDetectionMode, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/image-parameter/text-detection-mode.html
---


# TextDetectionMode

TextDetectionMode determines how to detect the text area. For tasks like barcode reading or border detection, the text part is not important; while for the task of text recognition, the results of detected text zone are mandatory.

## Example

```json
{
    "TextDetectionMode":{
        "Mode": "TDM_WORD",
        "Direction": "HORIZONTAL",
        "CharHeightRange": [1,1000,1],
        "MaxSpacingInALine": 10
    }
}
```

## Parameter Summary

Parameter TextDetectionMode consists of one or more of the following modes, each mode representing a different preprocessing algorithm:

### Child Parameters

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
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
        <td><b>Candidate Mode List</b><br>TDM_WORD
            <br>TDM_LINE
            <br>TDM_LAYOUT
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
        <td><b>Range</b><br>[0, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>TDM_LINE
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

#### Under BarcodeReaderTaskSetting

```json
{
    
}
```

#### Under LabelRecognizerTaskSetting

#### Under DocumentNormalizerTaskSetting

## Candidate Modes Introduction

### TDM_WORD



### TDM_LINE



### TDM_LAYOUT



## See Also
- [Capture Vision Template]()
- [Image Parameter]() 