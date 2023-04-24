---
layout: default-layout
Title: EnableAddonCode - Dynamsoft Barcode Reader Parameters
Description: The parameter EnableAddonCode of Dynamsoft Barcode Reader defines whether to identify addon code.
Keywords: EnableAddonCode , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/enable-addon-code.html
---

# EnableAddonCode

Parameter `EnableAddonCode` defines whether to identify addon code.

## Example

```json
{
    "EnableAddonCode": 1
}
```

## Parameter Summary

The structure of the `EnableAddonCode` is shown as follow:

| EnableAddonCode  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: do not identify addon code.
- 1: identify addon code.
- This parameter is valid only for EAN8/EAN13/UPCA/UPCE code formats.
