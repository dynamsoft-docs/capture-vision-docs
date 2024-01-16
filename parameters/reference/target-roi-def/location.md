---
layout: default-layout
title: Location - Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/target-roi-def/location.html
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
            "ReferenceTaskNameArray": ["A_task"],
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
            "ReferenceObjectType": "ROT_ATOMIC_OBJECT",
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

#### ReferenceTaskNameArray

Filter the reference object by specifying the reference task name array. 

| AtomicResultTypeArray Parameter Summary |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be one of the task in the reference TargetROIDef object array. |
| **Default Value**<br>null |

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

Parameter `Offset` is an object that defines how the location is offset from the `reference object` or the original image. It includes the following child parameters:

* ReferenceObjectOriginIndex
* ReferenceObjectType
* ReferenceXAxis
* ReferenceYAxis
* MeasuredByPercentage
* FirstPoint
* SecondPoint
* ThirdPoint
* FourthPoint

#### ReferenceObjectOriginIndex

Defines which point of the reference object will be set as the origin of the coordinate system.

| ReferenceObjectOriginIndex Parameter Details |
| :------------------- |
| **Type**<br>*int* |
| **Value Range**<br>[0,3] |
| **Default Value**<br>0 |

#### ReferenceObjectType

Defines which coordinate system to use when configuring offset parameters basd on the reference objects.

| ReferenceObjectType Parameter Details |
| :------------------- |
| **Type**<br>*String* |
| **Value Range**<br>"ROT_ATOMIC_OBJECT" or "ROT_WHOLE_IMAGE" |
| **Default Value**<br>"ROT_ATOMIC_OBJECT" |

#### ReferenceXAxis

Defines the x-axis of the coordinate system to use when configuring offset parameters basd on the reference objects. It includes the following child parameters:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Details</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">AxisType<br></td>
        <td><b>Description</b><br>The type of the axis.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Value Range</b><br>"AT_MIDPOINT_EDGE", "AT_EDGE", or "AT_ROTATION_OTHER_AXIS"
                <br>"AT_MIDPOINT_EDGE": Indicates connecting the midpoints of the reference object's opposite edges as the axis.
                <br>"AT_EDGE": Indicates using one of the reference object's edges as the axis.
                <br>"AT_ROTATION_OTHER_AXIS": Indicates deriving the current axis by rotating another reference axis.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>"AT_MIDPOINT_EDGE"
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">EdgeIndex<br></td>
        <td><b>Description</b><br>Define which edge of the reference object will be set as the x-axis of the coordinate system.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Value Range</b><br>0, 1, 2, 3
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Valid only when `AxisType` is "AT_EDGE"</b>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">RotationAngle<br></td>
        <td><b>Description</b><br>The counterclockwise rotation angle used to rotate the reference axis.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Value Range</b><br>[0, 180]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>90
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b>Valid only when `AxisType` is "AT_ROTATION_OTHER_AXIS".</b>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LengthReference<br></td>
        <td><b>Description</b><br>Defines the measurement benchmark.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Value Range</b><br>"LR_X", "LR_Y"
                <br>"LR_X": Indicates using the x-axis edge length as the standard length within the coordinate system.
                <br>"LR_Y": Indicates using the y-axis edge length as the standard length within the coordinate system .
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>"LR_X"
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Valid only when `AxisType` is "AT_MIDPOINT_EDGE" or "AT_EDGE"</b>
        </td>
    </tr>
</table>

#### ReferenceYAxis

Defines the y-axis of the coordinate system to use when configuring offset parameters basd on the reference objects. It includes the following child parameters:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Details</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">AxisType<br></td>
        <td><b>Description</b><br>The type of the axis.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Value Range</b><br>"AT_MIDPOINT_EDGE", "AT_EDGE", or "AT_ROTATION_OTHER_AXIS"
                <br>"AT_MIDPOINT_EDGE": Indicates connecting the midpoints of the reference object's opposite edges as the axis.
                <br>"AT_EDGE": Indicates using one of the reference object's edges as the axis.
                <br>"AT_ROTATION_OTHER_AXIS": Indicates deriving the current axis by rotating another reference axis.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>"AT_MIDPOINT_EDGE"
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">EdgeIndex<br></td>
        <td><b>Description</b><br>Define which edge of the reference object will be set as the y-axis of the coordinate system.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Value Range</b><br>0, 1, 2, 3
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>1
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Valid only when `AxisType` is "AT_EDGE"</b>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">RotationAngle<br></td>
        <td><b>Description</b><br>The clockwise rotation angle used to rotate the reference axis.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Value Range</b><br>[0, 180]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>90
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b>Valid only when `AxisType` is "AT_ROTATION_OTHER_AXIS".</b>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LengthReference<br></td>
        <td><b>Description</b><br>Defines the measurement benchmark.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Value Range</b><br>"LR_X", "LR_Y"
                <br>"LR_X": Indicates using the x-axis edge length as the standard length within the coordinate system.
                <br>"LR_Y": Indicates using the y-axis edge length as the standard length within the coordinate system .
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>"LR_Y"
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Valid only when `AxisType` is "AT_MIDPOINT_EDGE" or "AT_EDGE"</b>
        </td>
    </tr>
</table>

#### MeasuredByPercentage

Sets whether or not to use percentage to measure the points' coordinates.

| MeasuredByPercentage Parameter Details |
| :------------------- |
| **Type**<br>*int* |
| **Range**<br>0 or 1 |
| **Default Value**<br>1 |
| **Remarks**<br>0: not by percentage <br>1: by percentage |

#### FirstPoint

Specifies the top-left vertex of the ROI with two possible expression forms:

* `[X, Y]`: Represents the coordinates on the x and y axes. The expression in percentage for x and y is determined by parameter `MeasuredByPercentage`.
* `[X, Y, MeasuredXByPercentage, MeasuredYByPercentage]`: Includes independent control over whether the values for x and y are expressed in percentage. `MeasuredXByPercentage` determines if the x-value is in percentage, and `MeasuredYByPercentage` controls the y-value.

| FirstPoint Parameter Details |
| :------------------- |
| **Type**<br>*int[2]* or *int[4]* |
| **Default Value**<br>null |

#### SecondPoint

Specifies the top-right vertex of the ROI with two possible expression forms:

* `[X, Y]`: Represents the coordinates on the x and y axes. The expression in percentage for x and y is determined by parameter `MeasuredByPercentage`.
* `[X, Y, MeasuredXByPercentage, MeasuredYByPercentage]`: Includes independent control over whether the values for x and y are expressed in percentage. `MeasuredXByPercentage` determines if the x-value is in percentage, and `MeasuredYByPercentage` controls the y-value.

| FirstPoint Parameter Details |
| :------------------- |
| **Type**<br>*int[2]* or *int[4]* |
| **Default Value**<br>null |

#### ThirdPoint

Specifies the bottom-right vertex of the ROI with two possible expression forms:

* `[X, Y]`: Represents the coordinates on the x and y axes. The expression in percentage for x and y is determined by parameter `MeasuredByPercentage`.
* `[X, Y, MeasuredXByPercentage, MeasuredYByPercentage]`: Includes independent control over whether the values for x and y are expressed in percentage. `MeasuredXByPercentage` determines if the x-value is in percentage, and `MeasuredYByPercentage` controls the y-value.

| FirstPoint Parameter Details |
| :------------------- |
| **Type**<br>*int[2]* or *int[4]* |
| **Default Value**<br>null |

#### FourthPoint

Specifies the bottom-left vertex of the ROI with two possible expression forms:

* `[X, Y]`: Represents the coordinates on the x and y axes. The expression in percentage for x and y is determined by parameter `MeasuredByPercentage`.
* `[X, Y, MeasuredXByPercentage, MeasuredYByPercentage]`: Includes independent control over whether the values for x and y are expressed in percentage. `MeasuredXByPercentage` determines if the x-value is in percentage, and `MeasuredYByPercentage` controls the y-value.

| FirstPoint Parameter Details |
| :------------------- |
| **Type**<br>*int[2]* or *int[4]* |
| **Default Value**<br>null |

