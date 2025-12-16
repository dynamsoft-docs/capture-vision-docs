---
layout: default-layout
title: IncludeTrailingCheckDigit - Dynamsoft Barcode Reader Parameters
description: The parameter IncludeTrailingCheckDigit of Dynamsoft Barcode Reader defines whether to include the trailing check digit in the byte result.
keywords: IncludeTrailingCheckDigit, parameter reference, parameter
---

# IncludeTrailingCheckDigit

Parameter `IncludeTrailingCheckDigit` defines whether to include the trailing check digit in the byte result.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── IncludeTrailingCheckDigit
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "IncludeTrailingCheckDigit": 1
}
```

> [!NOTE]
> - This snippet shows only the `IncludeTrailingCheckDigit` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `IncludeTrailingCheckDigit` is shown as follow:

| IncludeTrailingCheckDigit  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: exclude.
- 1: include.
- This parameter is valid only for Code 128.
- Introduced in version 11.0.4000.
- Changed the default value to 0 from 1 in version 11.2.1000
