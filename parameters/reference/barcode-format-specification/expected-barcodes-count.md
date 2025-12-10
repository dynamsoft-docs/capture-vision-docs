---
layout: default-layout
title: ExpectedBarcodesCount - Dynamsoft Barcode Reader Parameters
description: The parameter ExpectedBarcodesCount of BarcodeFormatSpecification defines the expected number of barcodes for a specific format.
keywords: Expected barcodes count
---

# ExpectedBarcodesCount

Parameter `ExpectedBarcodesCount` of `BarcodeFormatSpecification` defines the expected number of barcodes for a specific format.

**Remarks**

- Introduced in version 11.2.1000.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── ExpectedBarcodesCount
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "ExpectedBarcodesCount": 0
}
```

> [!NOTE]
> - This snippet shows only the `ExpectedBarcodesCount` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| ExpectedBarcodesCount Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[1, 0x7fffffff] |
| **Default Value**<br>0x7fffffff |

