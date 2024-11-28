---
layout: default-layout
title: CornerAngleRange - Dynamsoft Document Normalizer Parameters
description: The parameter CornerAngleRange of Dynamsoft Document Normalizer is XXX.
keywords:
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# CornerAngleRange

Parameter `CornerAngleRange` specifies the range of angles (in degrees) of the extracted corners. The corners refer to the corners of a quad or document.

## Example

```json
{
    "CornerAngleRange":
        {
            "MinValue": 80,
            "MaxValue": 100
        }
}
```

## Parameter Summary

`CornerAngleRange` The range of a maximum and a minimum value of the angles.

### Child Parameters

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">MinValue</td>
        <td><b>Description</b><br>Sets the minimum interior angle.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,90]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>70
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">MaxValue</td>
        <td><b>Description</b><br>Sets the maximum interior angle.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[90,180]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>110</td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Please ensure that all interior angles of the target quadrilateral fall within the specified value range.
        <br>If the setting values doesn't meet the requirement ranges, an error will be raised.
        </td>
    </tr>
</table>

### Default Setting

If the `CornerAngleRange` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "CornerAngleRange" : 
        {
            "MaxValue" : 110,
            "MinValue" : 70
        }
}
```
