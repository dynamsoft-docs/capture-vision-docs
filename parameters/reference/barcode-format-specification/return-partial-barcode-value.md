---
layout: default-layout
title: ReturnPartialBarcodeValue - Dynamsoft Barcode Reader Parameters
description: The parameter ReturnPartialBarcodeValue of Dynamsoft Barcode Reader defines whether to return partial barcode value(s).
keywords: ReturnPartialBarcodeValue , parameter reference, parameter
---

# ReturnPartialBarcodeValue

`ReturnPartialBarcodeValue` defines whether to return partial barcode value(s).

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── ReturnPartialBarcodeValue
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "ReturnPartialBarcodeValue": 0
}
```

> [!NOTE]
> - This snippet shows only the `ReturnPartialBarcodeValue` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the`ReturnPartialBarcodeValue` is shown as follow:

| ReturnPartialBarcodeValue  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br> 1 |

**Remarks**

- 0: do not return partial barcode value(s).
- 1: return partial barcode value(s).
