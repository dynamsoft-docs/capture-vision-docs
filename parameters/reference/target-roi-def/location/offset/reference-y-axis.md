---
layout: default-layout
title:  Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needGenerateH3Content: true
---
## ReferenceYAxis

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
