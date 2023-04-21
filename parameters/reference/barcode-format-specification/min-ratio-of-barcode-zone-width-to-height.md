---
layout: default-layout
Title: MinRatioOfBarcodeZoneWidthToHeight - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for MinRatioOfBarcodeZoneWidthToHeight.
Keywords: MinRatioOfBarcodeZoneWidthToHeight , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/min-ratio-of-barcode-zone-width-to-height.html
---

# MinRatioOfBarcodeZoneWidthToHeight  

`MinRatioOfBarcodeZoneWidthToHeight` defines the minimum ratio (width/height as a percentage) of the barcode zone.
## Example


```json
{
    "MinRatioOfBarcodeZoneWidthToHeight": 100
}
```

## Parameter Summary
The structure of the`MinRatioOfBarcodeZoneWidthToHeight` is shown as follow:

| MinRatioOfBarcodeZoneWidthToHeight  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 10000] |
| **Default Value**<br> 0|


### Default Settings

If the `MinRatioOfBarcodeZoneWidthToHeight` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "MinRatioOfBarcodeZoneWidthToHeight": 0
}
```