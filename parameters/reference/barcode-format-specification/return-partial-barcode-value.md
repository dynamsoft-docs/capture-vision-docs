---
layout: default-layout
title: ReturnPartialBarcodeValue - Dynamsoft Barcode Reader Parameters
description: The parameter ReturnPartialBarcodeValue of Dynamsoft Barcode Reader defines whether to return partial barcode value(s).
keywords: ReturnPartialBarcodeValue , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/return-partial-barcode-value.html
---

# ReturnPartialBarcodeValue

`ReturnPartialBarcodeValue` defines whether to return partial barcode value(s).

## Example

```json
{
    "ReturnPartialBarcodeValue": 0
}
```

## Parameter Summary

The structure of the`ReturnPartialBarcodeValue` is shown as follow:

| ReturnPartialBarcodeValue  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br> 1 |

**Remarks**

- 0: do not return partial barcode value(s).
- 1: return partial barcode value(s).
