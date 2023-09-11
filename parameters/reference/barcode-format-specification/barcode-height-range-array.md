---
layout: default-layout
title: BarcodeHeightRangeArray - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeHeightRangeArray of Dynamsoft Barcode Reader defines the range of heights (in pixels) for barcodes searching and result filtering.
keywords: BarcodeHeightRangeArray  , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-height-range-array.html
---

# BarcodeHeightRangeArray

Parameter `BarcodeHeightRangeArray` defines the range of heights (in pixels) for barcodes searching and result filtering.

## Example

```json
{
    "BarcodeHeightRangeArray": 
    [
        {
            "MinValue": 100,
            "MaxValue": 200
        }
    ]
}
```

## Parameter Summary

Parameter `BarcodeHeightRangeArray` consist of a group of barcode height range objects. Each barcode angle range object includes the maximum and minimum value of the barcode height range.

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MinValue<br></td>
        <td><b>Description</b><br>Defines the MinValue of the barcode height range.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MaxValue<br></td>
        <td><b>Description</b><br>Defines the MaxValue of the barcode height range.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,0x7fffffff]
        </td>
    </tr>
</table>

### Default Settings

If the `BarcodeHeightRangeArray` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "BarcodeHeightRangeArray ": []
}
```
