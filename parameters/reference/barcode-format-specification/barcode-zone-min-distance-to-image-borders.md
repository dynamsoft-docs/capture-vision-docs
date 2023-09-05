---
layout: default-layout
title: BarcodeZoneMinDistanceToImageBorders - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeZoneMinDistanceToImageBorders of Dynamsoft Barcode Reader defines the minimum distance (in pixels) between the barcode zone and image borders.
keywords: BarcodeZoneMinDistanceToImageBorders , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-zone-min-distance-to-image-borders.html
---

# BarcodeZoneMinDistanceToImageBorders

Parameter `BarcodeZoneMinDistanceToImageBorders` defines the minimum distance (in pixels) between the barcode zone and image borders.

## Example

```json
{
    "BarcodeZoneMinDistanceToImageBorders": 1
}
```

## Parameter Summary

The structure of the `BarcodeZoneMinDistanceToImageBorders` is shown as follow:

| BarcodeZoneMinDistanceToImageBorders  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br> 0|

**Remarks**

- If a barcode region has been set, this parameter should not be used.
