---
layout: default-layout
title: ShortLineDetectionMode - Dynamsoft Capture Vision Parameters
description: The parameter ShortLineDetectionMode of Dynamsoft Capture Vision is for detecting short lines on an image.
keywords: ShortLineDetectionMode, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---


# ShortLineDetectionMode

Parameter `ShortLineDetectionMode` determines how to detect the short lines. For tasks like document detection, short line is very important and usually requires a stronger detection sensitivity to ensure enough short lines are captured.

## Example

```json
{
    "ShortlineDetectionMode":
    {
        "Mode": "SDM_GENERAL",
        "Sensitivity": 3
    }
}
```

## Parameter Summary

Parameter `ShortlineDetectionMode` includes a mode arguments shown as follow:

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
        <td><b>Candidate Mode List</b><br>SDM_GENERAL
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>SDM_GENERAL
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Sensitivity<br>(Optional)</td>
        <td><b>Description</b><br>Sets the sensitivity used for short line detection. A larger value means the library will take more effort to detect short lines.
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
        <br>SDM_GENERAL
        </td>
    </tr>
</table>

### Default Setting

If the `ShortlineDetectionMode` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "ShortlineDetectionMode":
    [
        {
            "Mode": "SDM_GENERAL",
            "Sensitivity": 3
        }
    ]
}
```

## Candidate Modes Introduction

### SDM_GENERAL

Detects short lines using the general algorithm. This mode has the following arguments for further customization.

**Available Mode Arguments:**

- Sensitivity
