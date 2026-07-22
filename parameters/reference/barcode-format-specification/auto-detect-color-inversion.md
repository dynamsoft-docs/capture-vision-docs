---
layout: default-layout
title: AutoDetectColorInversion - Dynamsoft Barcode Reader Parameters
description: The parameter AutoDetectColorInversion of Dynamsoft Barcode Reader defines whether to automatically detect and decode barcodes with inverted foreground and background colors.
keywords: AutoDetectColorInversion, inverted, parameter reference, parameter
---

# AutoDetectColorInversion

Parameter `AutoDetectColorInversion` defines whether to automatically detect and decode barcodes that have inverted foreground and background colors (i.e., light modules on a dark background) without requiring global grayscale inversion via `GrayscaleTransformationModes`.

**Remarks**

- Introduced in version 11.6.1000.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── AutoDetectColorInversion
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "BarcodeFormatIds": ["BF_DATAMATRIX"],
    "AutoDetectColorInversion": 0
}
```

> [!NOTE]
> - This snippet shows only the `AutoDetectColorInversion` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - The `BarcodeFormatIds` in the same `BarcodeFormatSpecification` determines which barcode formats this setting applies to.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `AutoDetectColorInversion` is shown as follow:

| AutoDetectColorInversion Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: Disabled. The SDK does not perform additional inverted-color detection at the barcode-candidate level. Whether normal (dark-on-light) or inverted (light-on-dark) barcodes can be decoded depends entirely on the [`GrayscaleTransformationModes`]({{ site.dcvb_parameters_reference }}image-parameter/grayscale-transformation-modes.html) setting.
- 1: Enabled. In addition to the behavior determined by `GrayscaleTransformationModes`, the SDK automatically detects whether a candidate barcode region has inverted colors and decodes it accordingly. This means both normal and inverted barcodes can be decoded regardless of the `GrayscaleTransformationModes` setting.

### Supported Barcode Formats

In the current version, the following barcode formats support automatic color-inversion detection:

| Barcode Format | Supported Since |
|---|---|
| `BF_DATAMATRIX` | v11.6.1000 |

Support for additional formats (e.g., QR Code, PDF417, Aztec) is planned for future releases.

### Difference from GrayscaleTransformationModes

This parameter works at the **candidate-barcode level** during decoding, which is fundamentally different from the **image-level** [`GrayscaleTransformationModes`]({{ site.dcvb_parameters_reference }}image-parameter/grayscale-transformation-modes.html):

| | `GrayscaleTransformationModes` | `AutoDetectColorInversion` |
|---|---|---|
| **Scope** | Entire image | Per candidate barcode region |
| **Timing** | Before localization | During localization |
| **Granularity** | Affects all barcode types globally | Per-format via `BarcodeFormatIds` |
| **Performance cost** | High (processes entire image twice when both `GTM_ORIGINAL` and `GTM_INVERTED` are set) | Low (only checks targeted candidate regions) |

**When to use which:**
- Use `AutoDetectColorInversion` when only certain barcode formats may be inverted, while other barcodes on the same image are normal. This is more efficient and precise.
- Use `GrayscaleTransformationModes` with `GTM_INVERTED` when the entire image has inverted colors, or when you need to handle inverted barcodes of formats not yet supported by `AutoDetectColorInversion`.
- The two parameters can be used together. `GrayscaleTransformationModes` is applied first at the image level, then `AutoDetectColorInversion` performs additional per-region detection during decoding.
