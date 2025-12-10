---
layout: default-layout
title:  Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needGenerateH3Content: true
---
# RegionFilteringCondition

One of the filter conditions. Filter the reference objects with the decoded barcode information. The parameter `RegionFilteringCondition` includes the following child parameters:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">RegionPredetectionMode</td>
        <td><b>Description</b><br>Filter the region by its RegionPredetectionMode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>
            "RPM_SKIP"<br>
            "RPM_AUTO"<br>
            "RPM_GENERAL"<br>
            "RPM_GENERAL_RGB_CONTRAST"<br>
            "RPM_GENERAL_GRAY_CONTRAST"<br>
            "RPM_GENERAL_HSV_CONTRAST"<br>
            "RPM_NEURAL_NETWORK"
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>"RPM_SKIP"
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">LabelIdArray</td>
        <td><b>Description</b><br>Filter the region by its LabelIdArray. Only available for the "RPM_NEURAL_NETWORK" mode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int[]</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>"RPM_NEURAL_NETWORK"
        </td>
    </tr>
</table>

Default Value

```json
"RegionFilteringCondition": null
```
