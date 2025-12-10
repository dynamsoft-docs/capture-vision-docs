---
layout: default-layout
title: BarcodeAngleRangeArray - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeAngleRangeArray of Dynamsoft Barcode Reader helps specify the encoding table used to code the Customer Information Field of Australian Post Customer Barcode.
keywords: BarcodeAngleRangeArray , parameter reference, parameter
---

# BarcodeAngleRangeArray

Parameter `BarcodeAngleRangeArray` defines the range of angles (in degrees) for barcodes searching and result filtering.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── BarcodeAngleRangeArray
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

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

> [!NOTE]
> - This snippet shows only the `BarcodeAngleRangeArray` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

Parameter `BarcodeAngleRangeArray` consist of a group of barcode rotation angle range objects. Each object includes the maximum and minimum value of the barcode rotation angle range.

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
