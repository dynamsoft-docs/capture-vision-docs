---
layout: default-layout
title:  Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needGenerateH3Content: true
---
# FrameFilteringCondition

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
