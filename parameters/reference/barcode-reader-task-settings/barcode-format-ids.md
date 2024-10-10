---
layout: default-layout
title: BarcodeFormatIds - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeFormatIds of Dynamsoft Barcode Reader defines the barcode formats to process.
keywords: Barcode format IDs
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/barcode-format-ids.html
---

# BarcodeFormatIds

Parameter `BarcodeFormatIds` defines the formats of the barcode to process. You can specify multiple barcode formats at one time. View enumeration [BarcodeFormats]({{site.dcvb_enums}}barcode-reader/barcode-format.html) for all supported barcode formats.

## Example

```json
{
    "BarcodeFormatIds": ["BF_ONED", "BF_DATAMATRIX"]
}
```

## Parameter Summary

| BarcodeFormatIds Parameter Summary |
| :--------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member of the array should be one of the BarcodeFormat enumeration member as a string. |
| **Default Value**<br>[ "BF_DEFAULT" ] |
