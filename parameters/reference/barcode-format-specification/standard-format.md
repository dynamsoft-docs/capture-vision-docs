---
layout: default-layout
title: StandardFormat - Dynamsoft Barcode Reader Parameters
description: The parameter StandardFormat of Dynamsoft Barcode Reader defines the standard barcode format.
keywords: StandardFormat , parameter reference, parameter
---

# StandardFormat

`StandardFormat` defines the standard barcode format.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── StandardFormat
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "StandardFormat": "BF_CODE128"
}
```

> [!NOTE]
> - This snippet shows only the `StandardFormat` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the`StandardFormat` is shown as follow:

| StandardFormat  Parameter Details |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>[BarcodeFormat]({{ site.dcvb_enums }}barcode-reader/barcode-format.html#barcodeformat) |
| **Default Value**<br> ""|
