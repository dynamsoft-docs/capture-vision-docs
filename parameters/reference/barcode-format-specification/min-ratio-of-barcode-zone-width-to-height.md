---
layout: default-layout
title: MinRatioOfBarcodeZoneWidthToHeight - Dynamsoft Barcode Reader Parameters
description: The parameter MinQuietZoneWidth of Dynamsoft Barcode Reader defines the minimum ratio (width/height as a percentage) of the barcode zone.
keywords: MinRatioOfBarcodeZoneWidthToHeight , parameter reference, parameter
---

# MinRatioOfBarcodeZoneWidthToHeight

Parameter `MinRatioOfBarcodeZoneWidthToHeight` defines the minimum ratio (width/height as a percentage) of the barcode zone.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── MinRatioOfBarcodeZoneWidthToHeight
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "MinRatioOfBarcodeZoneWidthToHeight": 100
}
```

> [!NOTE]
> - This snippet shows only the `MinRatioOfBarcodeZoneWidthToHeight` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `MinRatioOfBarcodeZoneWidthToHeight` is shown as follow:

| MinRatioOfBarcodeZoneWidthToHeight  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 10000] |
| **Default Value**<br> 0 |
