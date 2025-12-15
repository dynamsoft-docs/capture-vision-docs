---
layout: default-layout
title: BarcodeFormatIds - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeFormatIds defines which barcode formats a BarcodeFormatSpecification configuration applies to.
keywords: Barcode format IDs
---

# BarcodeFormatIds

Parameter `BarcodeFormatIds` specifies which barcode formats the current `BarcodeFormatSpecification` configuration applies to. You can specify multiple barcode formats at one time.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── BarcodeFormatIds
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "BarcodeFormatIds": ["BF_ONED", "BF_DATAMATRIX"]
}
```

> [!NOTE]
> - This snippet shows only the `BarcodeFormatIds` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| BarcodeFormatIds Parameter Details |
| :--------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each array element should be a string value from the `BarcodeFormat` enumeration. |
| **Default Value**<br>`["BF_ALL"]` |

**Remarks**

`BarcodeFormat` enumeration for all supported barcode formats:

{%- include barcode-format.md -%}
