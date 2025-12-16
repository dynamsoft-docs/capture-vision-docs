---
layout: default-layout
title: BarcodeZoneBarCountRangeArray - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeZoneBarCountRangeArray of Dynamsoft Barcode Reader defines the range of bar count of the barcode zone for barcodes searching.
keywords: BarcodeZoneBarCountRangeArray , parameter reference, parameter
---

# BarcodeZoneBarCountRangeArray

Parameter `BarcodeZoneBarCountRangeArray` defines the range of bar count of the barcode zone for barcodes searching.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── BarcodeZoneBarCountRangeArray
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

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

> [!NOTE]
> - This snippet shows only the `BarcodeZoneBarCountRangeArray` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

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
