---
layout: default-layout
title: BarcodeZoneMinDistanceToImageBorders - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeZoneMinDistanceToImageBorders of Dynamsoft Barcode Reader defines the minimum distance (in pixels) between the barcode zone and image borders.
keywords: BarcodeZoneMinDistanceToImageBorders , parameter reference, parameter
---

# BarcodeZoneMinDistanceToImageBorders

Parameter `BarcodeZoneMinDistanceToImageBorders` defines the minimum distance (in pixels) between the barcode zone and image borders.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── BarcodeZoneMinDistanceToImageBorders
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "BarcodeZoneMinDistanceToImageBorders": 1
}
```

> [!NOTE]
> - This snippet shows only the `BarcodeZoneMinDistanceToImageBorders` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `BarcodeZoneMinDistanceToImageBorders` is shown as follow:

| BarcodeZoneMinDistanceToImageBorders  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br> 0|

**Remarks**

- If a barcode region has been set, this parameter should not be used.
