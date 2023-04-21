---
layout: default-layout
Title: FindUnevenModuleBarcode - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for FindUnevenModuleBarcode.
Keywords: FindUnevenModuleBarcode , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/find-uneven-module-barcode.html
---

# FindUnevenModuleBarcode  

`FindUnevenModuleBarcode` defines whether to find barcodes with uneven barcode modules.
## Example


```json
{
    "FindUnevenModuleBarcode": 0
}
```

## Parameter Summary
The structure of the`FindUnevenModuleBarcode` is shown as follow:

| FindUnevenModuleBarcode  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br> 1|

**Remarks**
- 0: Do not find barcodes with uneven barcode modules.
- 1: Find barcodes with uneven barcode modules.

### Default Settings

If the `FindUnevenModuleBarcode` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "FindUnevenModuleBarcode": 1
}
```