---
layout: default-layout
title: LineAssemblyMode - Dynamsoft Capture Vision Parameters
description: The parameter LineAssemblyMode of Dynamsoft Capture Vision is for controlling how to assemble the lines.
keywords: LineAssemblyMode, assemble lines, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---


# LineAssemblyMode

Parameter `LineAssemblyMode` is for controlling how to assemble the lines.

## Example

```json
{
    "LineAssemblyMode": {
        "Mode": "LAM_GENERAL", 
        "Sensitivity": 3
    }
}
```

### Mode Arguments

Each `LineAssemblyMode` object consists a candidate mode name and a series of other mode arguments.

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
        <td><b>Candidate Mode List</b><br>"LAM_GENERAL"
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        <br>"LAM_GENERAL"
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Sensitivity<br>(Optional)</td>
        <td><b>Description</b><br>The sensitivity level used for line assembling.
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
        <td><b>Valid For</b><br>"LAM_GENERAL"
        </td>
    </tr>
</table>
