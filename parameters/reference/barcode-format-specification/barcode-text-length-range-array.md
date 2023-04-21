---
layout: default-layout
Title: BarcodeTextLengthRangeArray - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for BarcodeTextLengthRangeArray  .
Keywords: BarcodeTextLengthRangeArray  , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-text-length-range-array.html
---

# BarcodeTextLengthRangeArray  

`BarcodeTextLengthRangeArray` defines the range of barcode text length for barcodes searching and result filtering.
## Example

```json
{
    "BarcodeTextLengthRangeArray": [
    {
        "MinValue": 100,
        "MaxValue": 200
    }
    ]
}
```

## Parameter Summary

`BarcodeTextLengthRangeArray ` is not set by default which means there is no limitation on the barcode text length. The structure of the `BarcodeTextLengthRangeArray  ` is shown as follow:

| BarcodeTextLengthRangeArray  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*A JSON Object array: <br>defines MinValue and MaxValue of the barcode text length.* |
| **Range**<br>A number from [0, 0x7fffffff] |
| **Default Value**<br> |

### Default Settings

If the `BarcodeTextLengthRangeArray  ` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "BarcodeTextLengthRangeArray ": []
}
```