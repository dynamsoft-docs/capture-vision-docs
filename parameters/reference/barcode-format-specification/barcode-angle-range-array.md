---
layout: default-layout
Title: BarcodeAngleRangeArray - Dynamsoft Barcode Reader Parameters
Description: The parameter BarcodeAngleRangeArray of Dynamsoft Barcode Reader helps specify the encoding table used to code the Customer Information Field of Australian Post Customer Barcode.
Keywords: BarcodeAngleRangeArray , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-angle-range-array.html
---

# BarcodeAngleRangeArray

Parameter `BarcodeAngleRangeArray` defines the range of angles (in degrees) for barcodes searching and result filtering.

## Example

```json
{
    "BarcodeAngleRangeArray": 
    [
        {
            "MinValue": 100,
            "MaxValue": 200
        }
    ]
}
```

## Parameter Summary

Parameter `BarcodeAngleRangeArray` consist of a group of barcode rotation angle range objects. Each barcode angle range object includes the maximum and minimum value of the barcode rotation angle range.

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MinValue<br></td>
        <td><b>Description</b><br>Defines the MinValue of the barcode rotation angle range.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,360]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MaxValue<br></td>
        <td><b>Description</b><br>Defines the MaxValue of the barcode rotation angle range.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,360]
        </td>
    </tr>
</table>

### Default Settings

Parameter `BarcodeAngleRangeArray` is not set by default which means there is no limitation on the barcode angles. If the `BarcodeAngleRangeArray` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "BarcodeAngleRangeArray": []
}
```
