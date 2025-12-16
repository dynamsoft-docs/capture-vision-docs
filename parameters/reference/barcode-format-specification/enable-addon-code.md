---
layout: default-layout
title: EnableAddOnCode - Dynamsoft Barcode Reader Parameters
description: The parameter EnableAddOnCode of Dynamsoft Barcode Reader defines whether to identify addon code.
keywords: EnableAddOnCode , parameter reference, parameter
---

# EnableAddOnCode

Parameter `EnableAddOnCode` defines whether to identify addon code.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── EnableAddOnCode
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "EnableAddOnCode": 1
}
```

> [!NOTE]
> - This snippet shows only the `EnableAddOnCode` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `EnableAddOnCode` is shown as follow:

| EnableAddOnCode  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: do not identify addon code.
- 1: identify addon code.
- This parameter is valid only for EAN8/EAN13/UPCA/UPCE code formats.
