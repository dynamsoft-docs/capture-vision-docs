---
layout: default-layout
title: HasVerticalQuietZone - Dynamsoft Barcode Reader Parameters
description: The parameter Code128Subset of Dynamsoft Barcode Reader defines whether there is a sufficient vertical quiet zone above and below the barcode.
keywords: HasVerticalQuietZone , parameter reference, parameter
---

# HasVerticalQuietZone

Parameter `HasVerticalQuietZone` defines whether there is a sufficient vertical quiet zone above and below the barcode.

**Remarks**

- Introduced in version 11.2.1000.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── HasVerticalQuietzone
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "HasVerticalQuietZone": 0
}
```

> [!NOTE]
> - This snippet shows only the `HasVerticalQuietzone` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `HasVerticalQuietZone` is shown as follow:

| HasVerticalQuietZone  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br> 1|

**Remarks**

- 0: Do not require a sufficient vertical quiet zone above and below the barcode.
- 1: Require a sufficient vertical quiet zone above and below the barcode.
