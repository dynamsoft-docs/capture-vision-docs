---
layout: default-layout
title: MinResultConfidence - Dynamsoft Barcode Reader Parameters
description: The parameter MinResultConfidence of Dynamsoft Barcode Reader defines the minimum confidence of the result.
keywords: MinResultConfidence , parameter reference, parameter
---

# MinResultConfidence

`MinResultConfidence` defines the minimum confidence of the result.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── MinResultConfidence
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "MinResultConfidence": 0
}
```

> [!NOTE]
> - This snippet shows only the `MinResultConfidence` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `MinResultConfidence` is shown as follow:

| MinResultConfidence  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 100] |
| **Default Value**<br> 30|
