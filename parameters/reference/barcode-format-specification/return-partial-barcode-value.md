---
layout: default-layout
Title: ReturnPartialBarcodeValue - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for ReturnPartialBarcodeValue.
Keywords: ReturnPartialBarcodeValue , parameter reference, parameter
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
| **Default Value**<br> 1|

**Remarks**
- 0: do not return partial barcode value(s).
- 1: return partial barcode value(s).

### Default Settings

If the `ReturnPartialBarcodeValue` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "ReturnPartialBarcodeValue": 1
}
```