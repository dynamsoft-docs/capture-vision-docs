---
layout: default-layout
Title: BarcodeBytesLengthRangeArray - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for BarcodeBytesLengthRangeArray  .
Keywords: BarcodeBytesLengthRangeArray  , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-bytes-length-range-array.html
---

# BarcodeBytesLengthRangeArray  

`BarcodeBytesLengthRangeArray` defines the range of barcode bytes length for barcodes searching and result filtering.
## Example

```json
{
    "BarcodeBytesLengthRangeArray": [
    {
        "MinValue": 100,
        "MaxValue": 200
    }
    ]
}
```

## Parameter Summary

`BarcodeBytesLengthRangeArray ` is not set by default which means there is no limitation on the barcode bytes length. The structure of the `BarcodeBytesLengthRangeArray  ` is shown as follow:

| BarcodeBytesLengthRangeArray  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*A JSON Object array: <br>defines MinValue and MaxValue of the barcode bytes length.* |
| **Range**<br>A number from [0, 0x7fffffff] |
| **Default Value**<br> |

### Default Settings

If the `BarcodeBytesLengthRangeArray  ` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "BarcodeBytesLengthRangeArray ": []
}
```