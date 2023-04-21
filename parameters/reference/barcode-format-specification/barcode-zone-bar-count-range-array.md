---
layout: default-layout
Title: BarcodeZoneBarCountRangeArray   - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for BarcodeZoneBarCountRangeArray  .
Keywords: BarcodeZoneBarCountRangeArray , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-zone-bar-count-range-array.html
---

# BarcodeZoneBarCountRangeArray  

`BarcodeZoneBarCountRangeArray` defines the range of bar count of the barcode zone for barcodes searching.
## Example

```json
{
    "BarcodeZoneBarCountRangeArray": [
    {
        "MinValue": 1,
        "MaxValue": 8
    }
    ]
}
```

## Parameter Summary

`BarcodeZoneBarCountRangeArray` is not set by default which means there is no limitation on the bar count. The structure of the `BarcodeZoneBarCountRangeArray` is shown as follow:

| BarcodeZoneBarCountRangeArray  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*A JSON Object array: <br>defines MinValue and MaxValue of the bar count.* |
| **Range**<br>A number from [0, 0x7fffffff] |
| **Default Value**<br> "MinValue": 1<br>"MaxValue": 128|

### Default Settings

If the `BarcodeZoneBarCountRangeArray` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "BarcodeZoneBarCountRangeArray": [
    {
        "MinValue": 1,
        "MaxValue": 128
    }
    ]
}
```