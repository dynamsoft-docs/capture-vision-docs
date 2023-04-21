---
layout: default-layout
Title: BarcodeHeightRangeArray   - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for BarcodeHeightRangeArray  .
Keywords: BarcodeHeightRangeArray  , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-height-range-array.html
---

# BarcodeHeightRangeArray  

`BarcodeHeightRangeArray` defines the range of heights (in pixels) for barcodes searching and result filtering.
## Example

```json
{
    "BarcodeHeightRangeArray": [
    {
        "MinValue": 100,
        "MaxValue": 200
    }
    ]
}
```

## Parameter Summary

`BarcodeHeightRangeArray ` is not set by default which means there is no limitation on the barcode height. The structure of the `BarcodeHeightRangeArray  ` is shown as follow:

| BarcodeHeightRangeArray  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*A JSON Object array: <br>defines MinValue and MaxValue of the barcode height.* |
| **Range**<br>A number from [0, 0x7fffffff] |
| **Default Value**<br> |

### Default Settings

If the `BarcodeHeightRangeArray  ` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    {
    "BarcodeHeightRangeArray ": []
}
}
```