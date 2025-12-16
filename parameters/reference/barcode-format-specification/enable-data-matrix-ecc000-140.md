---
layout: default-layout
title: EnableDataMatrixECC000-140 - Dynamsoft Barcode Reader Parameters
description: The parameter EnableDataMatrixECC000-140 of Dynamsoft Barcode Reader defines whether to read Data Matrix ECC000-140 barcode.
keywords: Enable Data Matrix ECC000-140 , parameter reference, parameter
---

# EnableDataMatrixECC000-140

Parameter `EnableDataMatrixECC000-140` defines whether to read Data Matrix ECC000-140 barcode.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── EnableDataMatrixECC000-140
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "EnableDataMatrixECC000-140": 1
}
```

> [!NOTE]
> - This snippet shows only the `EnableDataMatrixECC000-140` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `EnableDataMatrixECC000-140` is shown as follow:

| EnableDataMatrixECC000-140  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: Do not read Data Matrix ECC000-140 barcode.
- 1: Read Data Matrix ECC000-140 barcode.
