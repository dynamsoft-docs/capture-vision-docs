---
layout: default-layout
title: EnableAddOnCode - Dynamsoft Barcode Reader Parameters
description: The parameter EnableAddOnCode of Dynamsoft Barcode Reader defines whether to identify addon code.
keywords: EnableAddOnCode , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/enable-addon-code.html
---

# EnableAddOnCode

Parameter `EnableAddOnCode` defines whether to identify addon code.

## Example

```json
{
    "EnableAddOnCode": 1
}
```

## Parameter Summary

The structure of the `EnableAddOnCode` is shown as follow:

| EnableAddOnCode  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: do not identify addon code.
- 1: identify addon code.
- This parameter is valid only for EAN8/EAN13/UPCA/UPCE code formats.
