---
layout: default-layout
title: RequireStartStopChars - Dynamsoft Barcode Reader Parameters
description: The parameter RequireStartStopChars of Dynamsoft Barcode Reader defines whether the start and/or stop characters are required when searching for common 1D barcodes.
keywords: RequireStartStopChars , parameter reference, parameter
---

# RequireStartStopChars

Parameter `RequireStartStopChars` defines whether the start and/or stop characters are required when searching for common 1D barcodes.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── RequireStartStopChars
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "RequireStartStopChars": 0
}
```

> [!NOTE]
> - This snippet shows only the `RequireStartStopChars` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the`RequireStartStopChars` is shown as follow:

| RequireStartStopChars  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br> 1 |

**Remarks**

- 0: start and/or stop characters are not required.
  >[!NOTE]
  > **Behavior changed in v11.0.4000**: In previous versions, this meant both start and stop characters were not required. Since v11.0.4000, it allows either or both to be missing.
- 1: start and stop characters are required.
