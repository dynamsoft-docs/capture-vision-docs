---
layout: default-layout
Title: MinQuietZoneWidth - Dynamsoft Barcode Reader Parameters
Description: The parameter MinQuietZoneWidth of Dynamsoft Barcode Reader defines the minimum width (in moduleSize) of the barcode quiet zone.
Keywords: MinQuietZoneWidth , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/min-quiet-zone-width.html
---

# MinQuietZoneWidth

`MinQuietZoneWidth` defines the minimum width (in moduleSize) of the barcode quiet zone.

## Example

```json
{
    "MinQuietZoneWidth": 1
}
```

## Parameter Summary

The structure of the `MinQuietZoneWidth` is shown as follow:

| MinQuietZoneWidth  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br> 4|

**Remarks**

- The unit is a multiplier of the barcode module size. For example, if barcode module is 2px and MinQuietZoneWidth is 4, then the width of quiet zone is 8px.
