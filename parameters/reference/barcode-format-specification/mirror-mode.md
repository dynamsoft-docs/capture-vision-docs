---
layout: default-layout
Title: MirrorMode - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for MirrorMode.
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

| MirrorMode  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>"MM_NORMAL"<br>"MM_MIRROR"<br>"MM_BOTH" |
| **Default Value**<br>|


## Candidate Modes Introduction

### MM_MIRROR
Decodes mirror barcodes only.

### MM_BOTH
Decodes both normal and mirror barcodes.

**Remarks**
- For QRCode, DataMatrix, PDF417, AZTEC, Micro QR Code, Micro PDF417, DotCode and Pharmacode Two-Track, "MM_BOTH" is the default setting.

### MM_NORMAL
Doesn't decode mirror barcodes.

**Remarks**
- For barcodes other than QRCode, DataMatrix, PDF417, AZTEC, Micro QR Code, Micro PDF417, DotCode and Pharmacode Two-Track, "MM_NORMAL" is the default setting.