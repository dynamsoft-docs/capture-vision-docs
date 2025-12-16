---
layout: default-layout
title: IncludeImpliedAI01 - Dynamsoft Barcode Reader Parameters
description: The parameter IncludeImpliedAI01 of Dynamsoft Barcode Reader defines whether to prepend the implied "01" at the beginning of the result bytes/text.
keywords: IncludeImpliedAI01, parameter reference, parameter
---

# IncludeImpliedAI01

Parameter `IncludeImpliedAI01` defines whether to prepend the implied "01" at the beginning of the result bytes/text.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── IncludeImpliedAi01
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "IncludeImpliedAI01": 1
}
```

> [!NOTE]
> - This snippet shows only the `IncludeImpliedAi01` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `IncludeImpliedAI01` is shown as follow:

| IncludeImpliedAI01  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: exclude.
- 1: include.
- This parameter is valid only for GS1_DATABAR/GS1_COMPOSITE code formats.

**Availability**

Introduced in version 11.0.4000.
