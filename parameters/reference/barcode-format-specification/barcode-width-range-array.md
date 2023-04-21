---
layout: default-layout
Title: BarcodeWidthRangeArray   - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for BarcodeWidthRangeArray  .
Keywords: BarcodeWidthRangeArray  , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-width-range-array.html
---

# BarcodeWidthRangeArray  

`BarcodeWidthRangeArray` defines the range of widths (in pixels) for barcodes searching and result filtering.
## Example

```json
{
    "BarcodeWidthRangeArray": [
    {
        "MinValue": 100,
        "MaxValue": 200
    }
    ]
}
```

## Parameter Summary

`BarcodeWidthRangeArray ` is not set by default which means there is no limitation on the barcode width. The structure of the `BarcodeWidthRangeArray  ` is shown as follow:

| BarcodeWidthRangeArray  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*A JSON Object array: <br>defines MinValue and MaxValue of the barcode width.* |
| **Range**<br>A number from [0, 0x7fffffff] |
| **Default Value**<br> |

### Default Settings

If the `BarcodeWidthRangeArray  ` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    {
    "BarcodeWidthRangeArray ": []
}
}
```