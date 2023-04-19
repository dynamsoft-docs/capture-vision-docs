---
layout: default-layout
Title: ReturnBarcodeZoneClarity - Dynamsoft Barcode Reader Parameters
Description: The parameter ReturnBarcodeZoneClarity of Dynamsoft Barcode Reader defines the returned coordinate type.
Keywords: Barcode zone clarity
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ReturnBarcodeZoneClarity

Parameter `ReturnBarcodeZoneClarity` defines whether to return the clarity of the barcode zone.

## Example

```json
{
    "ReturnBarcodeZoneClarity": 0
}
```

## Parameter Summary

| ReturnBarcodeZoneClarity Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: do not return the clarity of the barcode zone.
- 1: return the clarity of the barcode zone.
