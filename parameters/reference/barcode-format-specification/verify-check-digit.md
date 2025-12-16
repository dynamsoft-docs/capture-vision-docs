---
layout: default-layout
title: VerifyCheckDigit - Dynamsoft Barcode Reader Parameters
description: The parameter VerifyCheckDigit of Dynamsoft Barcode Reader specifies whether to verify the check digit in barcodes where this check digit is optional.
keywords: VerifyCheckDigit, parameter reference, parameter
---

# VerifyCheckDigit

Parameter `VerifyCheckDigit` specifies whether to verify the check digit in barcodes where this check digit is optional.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── VerifyCheckDigit
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "VerifyCheckDigit": 1
}
```

> [!NOTE]
> - This snippet shows only the `VerifyCheckDigit` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `VerifyCheckDigit` is shown as follow:

| VerifyCheckDigit  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- It is valid only for Code 11.
- 0: do not verify the check digit.
- 1: verify the check digit and if it does not match, no result will be returned. Do not set this parameter to 1 for barcodes without an optional check digit.
