---
layout: default-layout
title: Code128Subset - Dynamsoft Barcode Reader Parameters
description: The parameter Code128Subset of Dynamsoft Barcode Reader defines the subset of Code 128.
keywords: Code128Subset , parameter reference, parameter
---

# Code128Subset

Parameter `Code128Subset` defines the subset of Code 128.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── Code128Subset
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "Code128Subset": "A"
}
```

> [!NOTE]
> - This snippet shows only the `Code128Subset` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `Code128Subset` is shown as follow:

| Code128Subset  Parameter Details |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>"A"<br>"B"<br>"C" |
| **Default Value**<br> ""|
