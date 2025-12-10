---
layout: default-layout
title: MinQuietZoneWidth - Dynamsoft Barcode Reader Parameters
description: The parameter MinQuietZoneWidth of Dynamsoft Barcode Reader defines the minimum width (in moduleSize) of the barcode quiet zone.
keywords: MinQuietZoneWidth , parameter reference, parameter
---

# MinQuietZoneWidth

`MinQuietZoneWidth` defines the minimum width (in moduleSize) of the barcode quiet zone.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── MinQuietZoneWidth
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "MinQuietZoneWidth": 1
}
```

> [!NOTE]
> - This snippet shows only the `MinQuietZoneWidth` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `MinQuietZoneWidth` is shown as follow:

| MinQuietZoneWidth  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br> 4|

**Remarks**

- The unit is a multiplier of the barcode module size. For example, if barcode module is 2px and MinQuietZoneWidth is 4, then the width of quiet zone is 8px.
- This parameter is valid only for OneD barcode formats.

