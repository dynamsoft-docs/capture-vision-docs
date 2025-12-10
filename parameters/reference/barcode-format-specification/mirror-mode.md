---
layout: default-layout
title: MirrorMode - Dynamsoft Barcode Reader Parameters
description: The parameter MirrorMode of Dynamsoft Barcode Reader defines whether to decode mirrored barcodes.
keywords: MirrorMode , parameter reference, parameter
---

# MirrorMode

`MirrorMode` defines whether to decode mirrored barcodes.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── MirrorMode
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "MirrorMode": "MM_NORMAL"
}
```

> [!NOTE]
> - This snippet shows only the `MirrorMode` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the`MirrorMode` is shown as follow:

| MirrorMode Parameter Details |
| :--------------------------------- |
| **Type**<br>*String* |
| **Candidate Mode List**<br>MM_NORMAL<br>MM_MIRROR<br>MM_BOTH |

### Default Settings

Different barcode formats have different default MirrorMode settings:

- MM_BOTH: QRCode, DataMatrix, PDF417, AZTEC, Micro QR Code, Micro PDF417 and DotCode.
- MM_NORMAL: Other barcode formats

## Candidate Mode Introductions

### MM_MIRROR

Decodes mirror barcodes only.

### MM_BOTH

Decodes both normal and mirror barcodes.

### MM_NORMAL

Doesn't decode mirror barcodes.
