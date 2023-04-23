---
layout: default-layout
Title: BarcodeTextRegExPattern - Dynamsoft Barcode Reader Parameters
Description: The parameter BarcodeTextRegExPattern of Dynamsoft Barcode Reader defines the regular expression pattern of barcode text characters for barcodes searching and result filtering.
Keywords: BarcodeTextRegExPattern, parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-text-regex-pattern.html
---

# BarcodeTextRegExPattern

Parameter `BarcodeTextRegExPattern` defines the regular expression pattern of barcode text characters for barcodes searching and result filtering.

## Example

```json
{
    "BarcodeTextRegExPattern": " ^([*].+[*]|[+].+[+])$"
}
```

## Parameter Summary

`BarcodeTextRegExPattern` is set to an empty string by default which means there is no limitation on the barcode text characters. The structure of the `BarcodeTextRegExPattern` is shown as follow:

| BarcodeTextRegExPattern  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>N/A |
| **Default Value**<br>"" |
