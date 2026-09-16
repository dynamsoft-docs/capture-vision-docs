---
layout: default-layout
title: BarcodeTextRegExPattern - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeTextRegExPattern of Dynamsoft Barcode Reader defines the regular expression pattern of barcode text characters for barcodes searching and result filtering.
keywords: BarcodeTextRegExPattern, parameter reference, parameter
---

# BarcodeTextRegExPattern

Parameter `BarcodeTextRegExPattern` defines the regular expression pattern of barcode text characters for barcodes searching and result filtering.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── BarcodeTextRegExPattern
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters_reference }}barcode-format-specification/index.html) object

**Example:**

```json
{
    "BarcodeTextRegExPattern": " ^([*].+[*]|[+].+[+])$"
}
```

> [!NOTE]
> - This snippet shows only the `BarcodeTextRegExPattern` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters_reference }}barcode-format-specification/index.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters_reference }}index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters_reference }}index.html#minimal-valid-json-example)

## Parameter Details

`BarcodeTextRegExPattern` is set to an empty string by default which means there is no limitation on the barcode text characters. The structure of the `BarcodeTextRegExPattern` is shown as follow:

| BarcodeTextRegExPattern  Parameter Details |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>N/A |
| **Default Value**<br>"" |
