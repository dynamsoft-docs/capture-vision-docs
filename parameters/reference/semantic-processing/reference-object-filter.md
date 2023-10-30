---
layout: default-layout
title: ReferenceObjectFilter - Dynamsoft Capture Vision Semantic Processing object
description: The parameter ReferenceObjectFilter defines a group of filter conditions for figuring out the `reference objects`.
keywords: referenceobjectfilter
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# ReferenceObjectFilter

Parameter `ReferenceObjectFilter` is a group of filter conditions for figuring out the `reference objects`.

```json
"ReferenceObjectFilter" :
{
    "ReferenceTargetROIDefNameArray": ["TR_0", "TR_1"],
    "AtomicResultTypeArray" : ["ART_TEXT_LINE","ART_BARCODE","ART_FRAME","ART_TABLE_CELL"],
    "BarcodeFilteringCondition": 
    {
        "BarcodeFormatIds": ["BF_CODE39"], 
        "BarcodeTextRegExPattern": ".*b.*b.*b.*", 
        "RegionState": "default", 
    },
    "FrameFilteringCondition": 
    {
        "ImageDimensionRange": [16384,0x7fffffff],
        "AspectRatioRange": [1, 10000],
        "WidthRange": [1, 0x7fffffff],
        "HeightRange": [1, 0x7fffffff],
        "RegionState": "default",
    },
    "TextLineFilteringCondition":
    {
        "LineNumbers": "1,3-5",
        "LineStringRegExPattern": "Sodium[(\w| )]*",
        "RegionState": "default", 
    }
}
```

## ReferenceTargetROIDefNameArray

Filter the reference object by specifying `TargetROI` names.

| ReferenceTargetROIDefNameArray Parameter Summary |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be a name of `TargetROI` that defined in `TargetROIDefOptions`. |
| **Default Value**<br>null |

## AtomicResultTypeArray

Filter the reference object by specifying the type of atomic results. In the `TargetROIs` algorithm task can produce atomic results that can support the localization of the other `TargetROIs`.

| AtomicResultTypeArray Parameter Summary |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be one of the `AtomicResultType`, which are `ART_TEXT_LINE`, `ART_BARCODE`, `ART_FRAME`, `ART_TABLE_CELL`, `ART_GEOMETRY_LINE`, `ART_CORNER` and `ART_COLOUR_REGION` |
| **Default Value**<br>["ART_TEXT_LINE","ART_BARCODE","ART_FRAME"] |

## BarcodeFilteringCondition

One of the filter conditions. Filter the reference objects with the decoded barcode information. The parameter `BarcodeFilteringCondition` includes the following child parameters:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">BarcodeFormatIds</td>
        <td><b>Description</b><br>Filter the reference objects by the barcode formats.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String[]</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>Each member of the array should be one of the BarcodeFormatIds as a string.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">BarcodeTextRegExPattern</td>
        <td><b>Description</b><br>Filter the reference objects by the barcode text with a RegEx string.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
</table>

## FrameFilteringCondition

One of the filter conditions. Filter the reference objects with the frame information. The parameter `FrameFilteringCondition` includes the following child parameters:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">ImageDimensionRange</td>
        <td><b>Description</b><br>Filter the reference objects by the dimension of their original images.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int[2]</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>[16384,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">AspectRatioRange</td>
        <td><b>Description</b><br>Filter the reference objects by the aspect ratio of their original images.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int[2]</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>[1, 10000]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">WidthRange</td>
        <td><b>Description</b><br>Filter the reference objects by the width of their original images.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int[2]</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>[1, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">HeightRange</td>
        <td><b>Description</b><br>Filter the reference objects by the height of their original images.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int[2]</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>[1, 0x7fffffff]
        </td>
    </tr>
</table>

## TextLineFilteringCondition

One of the filter conditions. Filter the reference objects with the text line content. The parameter `TextLineFilteringCondition` includes the following child parameters:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LineNumbers</td>
        <td><b>Description</b><br>Filter the reference objects by the line numbers.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string of one or more of the following data, separated by commas:<br>1. One int value which represents a specified line index;<br>2. One Expression, start index and stop index connected with ""-"", which represents a specified line index range.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>(1) The value is 1-based.<br>(2) "" represents all lines.<br>(3) The processed of the not specified text lines will implement the default settings.<br>(4) If the line number you specified doesn't exist, the library will ignore it.
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">LineStringRegExPattern</td>
        <td><b>Description</b><br>Filter the reference objects by the content of the text line with a RegEx string.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
</table>
