---
layout: default-layout
title: ShortlineDetectionMode - Dynamsoft Capture Vision Parameters
description: The parameter ShortlineDetectionMode of Dynamsoft Capture Vision is for controlling how to detect the shortlines.
keywords: ShortlineDetectionMode, short lines, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---


# ShortlineDetectionMode

Parameter `ShortlineDetectionMode` is for controlling how to detect the shortlines.

## Example

```json
{
    "ShortlineDetectionMode": {
        "Mode": "SDM_GENERAL", 
        "Sensitivity": 3
    }
}
```

### Mode Arguments

Each `ShortlineDetectionMode` object consists a candidate mode name and a series of other mode arguments.

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
        <td><b>Candidate Mode List</b><br>"SDM_GENERAL"
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        <br>"SDM_GENERAL"
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Sensitivity<br>(Optional)</td>
        <td><b>Description</b><br>The sensitivity level used for short line detection.
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[1, 9]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>3 for BarcodeReader Task.<br>6 for DocumentNormalizer Task
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>"SDM_GENERAL"
        </td>
    </tr>
</table>
