---
layout: default-layout
title: LineAssemblyMode - Dynamsoft Capture Vision Parameters
description: The parameter LineAssemblyMode of Dynamsoft Capture Vision is for assembling short lines.
keywords: LineAssemblyMode, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---


# LineAssemblyMode

Parameter `LineAssemblyMode` determines how to assemble the short lines. For tasks like document detection, short line is very important and usually requires a stronger assembling sensitivity to ensure enough lines are captured.

## Example

```json
{
    "LineAssemblyMode":
    {
        "Mode": "LAM_GENERAL",
        "Sensitivity": 3
    }
}
```

## Parameter Summary

Parameter `LineAssemblyMode` includes a mode arguments shown as follow:

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
        <td><b>Candidate Mode List</b><br>LAM_GENERAL
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>LAM_GENERAL
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Sensitivity<br>(Optional)</td>
        <td><b>Description</b><br>Sets the sensitivity used for short line assembling. A larger value means the library will take more effort to assemble short lines.
        </td>
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
        <td><b>Valid For</b><br>
        <br>LAM_GENERAL
        </td>
    </tr>
</table>

### Default Setting

If the `LineAssemblyMode` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "LineAssemblyMode":
    [
        {
            "Mode": "LAM_GENERAL",
            "Sensitivity": 6
        }
    ]
}
```

## Candidate Modes Introduction

### LAM_GENERAL

Assemble short lines using the general algorithm. This mode has the following arguments for further customization.

**Available Mode Arguments:**

- Sensitivity
