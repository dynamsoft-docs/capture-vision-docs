---
layout: default-layout
title: BarcodeFormatSpecificationNameArray - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeFormatSpecificationNameArray of Dynamsoft Barcode Reader defines the collection of BarcodeFormatSpecification object names
keywords: BarcodeFormatSpecification, BarcodeReaderTaskSetting
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BarcodeFormatSpecificationNameArray

Parameter `BarcodeFormatSpecificationNameArray` defines the collection of BarcodeFormatSpecification object names, used to refer to the `BarcodeFormatSpecification` objects

## Example

```json
{
    "BarcodeFormatSpecificationNameArray": ["bfs_default"]
}
```

## Parameter Summary

| BarcodeFormatSpecificationNameArray Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element is the name of a `BarcodeFormatSpecification` object. |
| **Default Value**<br>null |
| **Remarks**<br>If `BarcodeFormatSpecificationNameArray` is not specified or null, a default configuration will be applied.|
