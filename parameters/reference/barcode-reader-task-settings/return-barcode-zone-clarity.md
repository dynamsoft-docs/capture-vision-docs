---
layout: default-layout
title: ReturnBarcodeZoneClarity - Dynamsoft Barcode Reader Parameters
description: The parameter ReturnBarcodeZoneClarity of Dynamsoft Barcode Reader defines the returned coordinate type.
keywords: Barcode zone clarity
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/return-barcode-zone-clarity.html
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
