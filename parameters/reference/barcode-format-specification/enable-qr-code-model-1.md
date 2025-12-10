---
layout: default-layout
title: EnableQRCodeModel1 - Dynamsoft Barcode Reader Parameters
description: The parameter EnableQRCodeModel1 of Dynamsoft Barcode Reader defines whether to read QR code model 1.
keywords: EnableQRCodeModel1 , parameter reference, parameter
---

# EnableQRCodeModel1

Parameter `EnableQRCodeModel1` defines whether to read QR code model 1.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── EnableQRCodeModel1
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "EnableQRCodeModel1": 1
}
```

> [!NOTE]
> - This snippet shows only the `EnableQRCodeModel1` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `EnableQRCodeModel1` is shown as follow:

| EnableQRCodeModel1  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: Do not read QR code model 1.
- 1: Read QR code model 1.
