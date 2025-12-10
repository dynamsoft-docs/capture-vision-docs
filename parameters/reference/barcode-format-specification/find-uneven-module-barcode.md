---
layout: default-layout
title: FindUnevenModuleBarcode - Dynamsoft Barcode Reader Parameters
description: The parameter Code128Subset of Dynamsoft Barcode Reader defines whether to find barcodes with uneven barcode modules.
keywords: FindUnevenModuleBarcode , parameter reference, parameter
---

# FindUnevenModuleBarcode

Parameter `FindUnevenModuleBarcode` defines whether to find barcodes with uneven barcode modules.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── FindUnevenModuleBarcode
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "FindUnevenModuleBarcode": 0
}
```

> [!NOTE]
> - This snippet shows only the `FindUnevenModuleBarcode` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `FindUnevenModuleBarcode` is shown as follow:

| FindUnevenModuleBarcode  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br> 1|

**Remarks**

- 0: Do not find barcodes with uneven barcode modules.
- 1: Find barcodes with uneven barcode modules.
