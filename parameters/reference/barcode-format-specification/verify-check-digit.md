---
layout: default-layout
title: VerifyCheckDigit - Dynamsoft Barcode Reader Parameters
description: The parameter VerifyCheckDigit of Dynamsoft Barcode Reader specifies whether to verify the check digit in barcodes where this check digit is optional.
keywords: VerifyCheckDigit, parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/verify-check-digit.html
---

# VerifyCheckDigit

Parameter `VerifyCheckDigit` specifies whether to verify the check digit in barcodes where this check digit is optional.

## Example

```json
{
    "VerifyCheckDigit": 1
}
```

## Parameter Summary

The structure of the `VerifyCheckDigit` is shown as follow:

| VerifyCheckDigit  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- It is valid only for Code 11.
- 0: do not verify the check digit.
- 1: verify the check digit and if it does not match, no result will be returned. Do not set this parameter to 1 for barcodes without an optional check digit.
