---
layout: default-layout
title: PatchCodeSearchingMargins - Dynamsoft Barcode Reader Parameters
description: The parameter PatchCodeSearchingMargins of Dynamsoft Barcode Reader defines the patch code searching margins.
keywords: PatchCodeSearchingMargins , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/patch-code-searching-margins.html
---

# PatchCodeSearchingMargins

Parameter `PatchCodeSearchingMargins` defines the patch code searching margins.

## Example

```json
{
    "PatchCodeSearchingMargins" : 
    {
        "Bottom" : 20,
        "Left" : 20,
        "MeasuredByPercentage" : 1,
        "Right" : 20,
        "Top" : 20
    }
}
```

## Parameter Summary

Parameter `PatchCodeSearchingMargins` is set by a patch code searching margins object. The patch code searching margins object includes a series of child parameters to define the top, bottom, left, right margins and how they are measured.

### Child Parameters

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MeasuredByPercentage<br></td>
        <td><b>Description</b><br>Defines whether to measure the margins by percentage.<br>1: measure by percentage.<br>0: do not measure by percentage.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,1]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Top<br></td>
        <td><b>Description</b><br>Defines the margin-top.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>When MeasureByPercentage = 1: [0,50]<br>When MeasureByPercentage = 0: [0,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Bottom<br></td>
        <td><b>Description</b><br>Defines the margin-bottom.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>When MeasureByPercentage = 1: [0,50]<br>When MeasureByPercentage = 0: [0,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Left<br></td>
        <td><b>Description</b><br>Defines the margin-left.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>When MeasureByPercentage = 1: [0,50]<br>When MeasureByPercentage = 0: [0,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Right<br></td>
        <td><b>Description</b><br>Defines the margin-right.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>When MeasureByPercentage = 1: [0,50]<br>When MeasureByPercentage = 0: [0,0x7fffffff]
        </td>
    </tr>
</table>

### Default Setting

If the `PatchCodeSearchingMargins` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "PatchCodeSearchingMargins" : 
    {
        "Bottom" : 20,
        "Left" : 20,
        "MeasuredByPercentage" : 1,
        "Right" : 20,
        "Top" : 20
    }
}
```
