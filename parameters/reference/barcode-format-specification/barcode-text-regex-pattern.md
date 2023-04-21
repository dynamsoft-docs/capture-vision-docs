---
layout: default-layout
Title: BarcodeTextRegExPattern - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for BarcodeTextRegExPattern.
Keywords: BarcodeTextRegExPattern, parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/barcode-text-regex-pattern.html
---

# BarcodeTextRegExPattern  

`BarcodeTextRegExPattern` defines the regular expression pattern of barcode text characters for barcodes searching and result filtering.
## Example

```json
{
    "BarcodeTextRegExPattern": " ^([*].+[*]|[+].+[+])$"
}
```

## Parameter Summary

`BarcodeTextRegExPattern ` is set to an empty string by default which means there is no limitation on the barcode text characters. The structure of the `BarcodeTextRegExPattern  ` is shown as follow:

| BarcodeTextRegExPattern  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>N/A |
| **Default Value**<br>"" |

### Default Settings

If the `BarcodeTextRegExPattern  ` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "BarcodeTextRegExPattern ": ""
}
```