---
layout: default-layout
title: BarcodeZoneBarCountRangeArray - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeZoneBarCountRangeArray of Dynamsoft Barcode Reader defines the range of bar count of the barcode zone for barcodes searching.
keywords: BarcodeZoneBarCountRangeArray , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BarcodeZoneBarCountRangeArray

Parameter `BarcodeZoneBarCountRangeArray` defines the range of bar count of the barcode zone for barcodes searching.

## Example

```json
{
    "BarcodeZoneBarCountRangeArray": [
        {
            "MinValue": 1,
            "MaxValue": 8
        }
    ]
}
```

## Parameter Summary

Parameter `BarcodeZoneBarCountRangeArray` consist of a group of barcode zone bar count range objects. Each object includes the maximum and minimum value of the barcode zone bar count range.

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MinValue<br></td>
        <td><b>Description</b><br>Defines the MinValue of the barcode zone bar count range.</td>
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
        <td><b>Description</b><br>Defines the MaxValue of the barcode zone bar count range.</td>
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

If the `BarcodeZoneBarCountRangeArray` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "BarcodeZoneBarCountRangeArray": [
    {
        "MinValue": 1,
        "MaxValue": 128
    }
    ]
}
```
