---
layout: default-layout
title:  Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# BarcodeFilteringCondition

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
