---
layout: default-layout
title: BarcodeZoneWidthToHeightRatioRangeArray - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeZoneWidthToHeightRatioRangeArray of Dynamsoft Barcode Reader defines the allowed width-to-height ratio range of the barcode zone for barcode searching.
keywords: BarcodeZoneWidthToHeightRatioRangeArray, parameter reference, parameter
---

# BarcodeZoneWidthToHeightRatioRangeArray

Parameter `BarcodeZoneWidthToHeightRatioRangeArray` defines the allowed width-to-height ratio range of the barcode zone for barcode searching.

**Remarks**

- Introduced in version 11.4.1000.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── BarcodeZoneWidthToHeightRatioRangeArray
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "BarcodeZoneWidthToHeightRatioRangeArray": [
        {
            "MinValue": 100,
            "MaxValue": 200
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `BarcodeZoneWidthToHeightRatioRangeArray` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

Parameter `BarcodeZoneWidthToHeightRatioRangeArray` consists of a group of width-to-height ratio range objects. Each object includes the minimum and maximum value of the ratio range, expressed as a percentage (width/height × 100).

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MinValue<br></td>
        <td><b>Description</b><br>Defines the minimum width-to-height ratio of the barcode zone, expressed as a percentage.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 10000]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MaxValue<br></td>
        <td><b>Description</b><br>Defines the maximum width-to-height ratio of the barcode zone, expressed as a percentage.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 10000]
        </td>
    </tr>
</table>

### Default Settings

If the `BarcodeZoneWidthToHeightRatioRangeArray` is not configured in your template file, the following settings will be used as the default settings. An empty array means no restriction on the width-to-height ratio.

```json
{
    "BarcodeZoneWidthToHeightRatioRangeArray": []
}
```
