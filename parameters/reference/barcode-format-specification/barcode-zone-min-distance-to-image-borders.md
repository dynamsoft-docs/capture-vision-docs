---
layout: default-layout
Title: BarcodeZoneMinDistanceToImageBorders - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for BarcodeZoneMinDistanceToImageBorders  .
Keywords: BarcodeZoneMinDistanceToImageBorders , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-zone-min-distance-to-image-borders.html
---

# BarcodeZoneMinDistanceToImageBorders  

`BarcodeZoneMinDistanceToImageBorders` defines the minimum distance (in pixels) between the barcode zone and image borders.
## Example


```json
{
    "BarcodeZoneMinDistanceToImageBorders": 1
}
```


## Parameter Summary
The structure of the`BarcodeZoneMinDistanceToImageBorders` is shown as follow:

| BarcodeZoneMinDistanceToImageBorders  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br> 0|

**Remarks**  
- If a barcode region has been set, this parameter should not be used.

### Default Settings

If the `BarcodeZoneMinDistanceToImageBorders` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "BarcodeZoneMinDistanceToImageBorders": 0
}
```