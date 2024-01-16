---
layout: default-layout
title: Location - Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/target-roi-def/location-v2.0.30.html
---

# Location

Parameter `Location` defines the location of the TargetROI with `reference objects` filter conditions and `offset` parameters.

## Example

```json
{
    "Location": 
    {
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
            "TableCellFilteringCondition":
            {
                "RowNumbers": "1,3,5", 
                "ColNumbers": "1", 
                "RegionState": "default", 
            },
            "TextLineFilteringCondition":
            {
                "LineNumbers": "1,3-5",
                "LineStringRegExPattern": "Sodium[(\w| )]*",
                "RegionState": "default", 
            }
        },
        "Offset": {
            "ReferenceObjectOriginIndex": 0,
            "ReferenceObjectSizeType": "default",
            "MeasuredByPercentage" : 1,
            "FirstPoint" : [ 0, 0 ],
            "SecondPoint" : [ 100, 0 ],
            "ThirdPoint" : [ 100, 100 ],
            "FourthPoint" : [ 0, 100 ],
        }
    }
}
```

## Parameter Summary

### ReferenceObjectFilter

Parameter `ReferenceObjectFilter` is a group of filter conditions for figuring out the `reference objects`.

#### ReferenceTargetROIDefNameArray

Filter the reference object by specifying `TargetROI` names.

| ReferenceTargetROIDefNameArray Parameter Summary |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be a name of `TargetROI` that defined in `TargetROIDefOptions`. |
| **Default Value**<br>null |

#### AtomicResultTypeArray

Filter the reference object by specifying the type of atomic results. In the `TargetROIs` algorithm task can produce atomic results that can support the localization of the other `TargetROIs`.

| AtomicResultTypeArray Parameter Summary |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be one of the `AtomicResultType`, which are `ART_TEXT_LINE`, `ART_BARCODE`, `ART_FRAME`, `ART_TABLE_CELL`, `ART_GEOMETRY_LINE`, `ART_CORNER` and `ART_COLOUR_REGION` |
| **Default Value**<br>["ART_TEXT_LINE","ART_BARCODE","ART_FRAME"] |

#### BarcodeFilteringCondition

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

#### FrameFilteringCondition

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
        <br><br><i>Aspect Ratio = BoundingRectHeight/BoundingRectWidth * 100</i><br><br>[MinAspectRatio, MaxAspectRatio]
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

#### TextLineFilteringCondition

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

### Offset

Parameter `Offset` is an object that defines how the location is offset from the `reference object` or the original image.

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">ReferenceObjectOriginIndex<br></td>
        <td><b>Description</b><br>Define which point of the reference object will be set as the origin of the coordinate system.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,3]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">ReferenceObjectSizeType<br></td>
        <td><b>Description</b><br>Define which coordinate system to use when configuring offset parameters basd on the reference objects.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>"default" or "wholeimage"
                <br>"default": Create the offset coordinate system based on the reference object.
                <br>"wholeimage": Create the offset coordinate system based on the original image.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>"default"
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">MeasuredInPercentage<br></td>
        <td><b>Description</b><br>Set whether or not to use percentage to measure the points' coordinates.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>0 or 1
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>1
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">FirstPoint<br></td>
        <td><b>Description</b><br>The top-left vertex of the ROI.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int[2]</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>When MeasureByPercentage = 1: 
            <br>If your ReferenceObjectSizeType is "default", the coordinate is measured based on the size of the <b>reference object</b>.
            <br>If your ReferenceObjectSizeType is "wholeimage", the coordinate is measured based on the size of the <b>TargetROI of the reference object.</b>
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">SecondPoint<br></td>
        <td><b>Description</b><br>The top-right vertex of the ROI.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int[2]</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>When MeasureByPercentage = 1:
            <br>If your ReferenceObjectSizeType is "default", the coordinate is measured based on the size of the <b>reference object</b>.
            <br>If your ReferenceObjectSizeType is "wholeimage", the coordinate is measured based on the size of the <b>TargetROI of the reference object.</b>
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">ThirdPoint<br></td>
        <td><b>Description</b><br>The bottom-right vertex of the ROI.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int[2]</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>When MeasureByPercentage = 1:
            <br>If your ReferenceObjectSizeType is "default", the coordinate is measured based on the size of the <b>reference object</b>.
            <br>If your ReferenceObjectSizeType is "wholeimage", the coordinate is measured based on the size of the <b>TargetROI of the reference object.</b>
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">FourthPoint<br></td>
        <td><b>Description</b><br>The bottom-left vertex of the ROI.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int[2]</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>When MeasureByPercentage = 1:
            <br>If your ReferenceObjectSizeType is "default", the coordinate is measured based on the size of the <b>reference object</b>.
            <br>If your ReferenceObjectSizeType is "wholeimage", the coordinate is measured based on the size of the <b>TargetROI of the reference object.</b>
        </td>
    </tr>
</table>
