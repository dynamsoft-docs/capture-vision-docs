---
layout: default-layout
title: IncludeTrailingCheckDigit - Dynamsoft Barcode Reader Parameters
description: The parameter IncludeTrailingCheckDigit of Dynamsoft Barcode Reader defines whether to include the trailing check digit in the byte result.
keywords: IncludeTrailingCheckDigit, parameter reference, parameter
---

# IncludeTrailingCheckDigit

Parameter `IncludeTrailingCheckDigit` defines whether to include the trailing check digit in the byte result.

## Example

```json
{
    "IncludeTrailingCheckDigit": 1
}
```

## Parameter Summary

The structure of the `IncludeTrailingCheckDigit` is shown as follow:

| IncludeTrailingCheckDigit  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>1 |

**Remarks**

- 0: exclude.
- 1: include.
- This parameter is valid only for Code 128.

**Availability**

Introduced in version 11.0.4000.