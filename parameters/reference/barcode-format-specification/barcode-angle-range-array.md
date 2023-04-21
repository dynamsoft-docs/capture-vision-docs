---
layout: default-layout
Title: BarcodeAngleRangeArray - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for BarcodeAngleRangeArray .
Keywords: BarcodeAngleRangeArray , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-angle-range-array.html
---

# BarcodeAngleRangeArray

Parameter `BarcodeAngleRangeArray` defines the range of angles (in degrees) for barcodes searching and result filtering.

## Example

```json
{
    "BarcodeAngleRangeArray": 
    [
        {
            "MinValue": 100,
            "MaxValue": 200
        }
    ]
}
```

## Parameter Summary

`BarcodeAngleRangeArray` is not set by default which means there is no limitation on the barcode angles. The structure of the `BarcodeAngleRangeArray ` is shown as follow:

| BarcodeAngleRangeArray Parameter Summary |
| :--------------------------------- |
| **Type**<br>*A JSON Object array: <br>defines MinValue and MaxValue of the barcode angle.* |
| **Range**<br>A number from [0, 360] |
| **Default Value**<br> |

### Default Settings

If the `BarcodeAngleRangeArray ` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "BarcodeAngleRangeArray": []
}
```
