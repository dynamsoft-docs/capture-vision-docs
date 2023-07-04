---
layout: default-layout
Title: MirrorMode - Dynamsoft Barcode Reader Parameters
Description: The parameter MirrorMode of Dynamsoft Barcode Reader defines whether to decode mirrored barcodes.
Keywords: MirrorMode , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/mirror-mode.html
---

# MirrorMode

`MirrorMode` defines whether to decode mirrored barcodes.

## Example

```json
{
    "MirrorMode": "MM_NORMAL"
}
```

## Parameter Summary

The structure of the`MirrorMode` is shown as follow:

| MirrorMode Parameter Summary |
| :--------------------------------- |
| **Type**<br>*String* |
| **Candidate Mode List**<br>MM_NORMAL<br>MM_MIRROR<br>MM_BOTH |

### Default Settings

Different barcode formats have different default MirrorMode settings:

- MM_BOTH: QRCode, DataMatrix, PDF417, AZTEC, Micro QR Code, Micro PDF417, DotCode and Pharmacode Two-Track.
- MM_NORMAL: Other barcode formats

## Candidate Modes Introduction

### MM_MIRROR

Decodes mirror barcodes only.

### MM_BOTH

Decodes both normal and mirror barcodes.

### MM_NORMAL

Doesn't decode mirror barcodes.
