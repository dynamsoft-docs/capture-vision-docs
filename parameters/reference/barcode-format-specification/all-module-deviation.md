---
layout: default-layout
title: AllModuleDeviation - Dynamsoft Barcode Reader Parameters
description: The parameter AllModuleDeviation of Dynamsoft Barcode Reader specifies the width deviation value (in moduleSize) of a non-standard 1D barcode type relative to the standard barcode width.
keywords: AllModuleDeviation, parameter reference, parameter
---

# AllModuleDeviation

Parameter `AllModuleDeviation` specifies the width deviation value (in moduleSize) of a non-standard 1D barcode type relative to the standard barcode width.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── AllModuleDeviation
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "AllModuleDeviation": 1
}
```

> [!NOTE]
> - This snippet shows only the `AllModuleDeviation` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The unit defined in Parameter `AllModuleDeviation` is barcode module size. For example, if the standard barcode module size is 2px and `AllModuleDeviation` is 1, then the non-standard barcode module size is 4px. The structure of the `AllModuleDeviation` is shown as follow:

| AllModuleDeviation Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br>0 |
