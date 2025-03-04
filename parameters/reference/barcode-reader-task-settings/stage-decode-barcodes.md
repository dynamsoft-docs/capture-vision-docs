---
layout: default-layout
title: DecodeBarcodesStage - Dynamsoft Barcode Reader Parameters
description: This page defines DecodeBarcodesStage object under the BarcodeDecodingSection.
keywords: DecodeBarcodesStage
---

# DecodeBarcodesStage

The `DecodeBarcodesStage` defines the stage that extracts and interprets barcode data from the localized barcode regions.

## Example

```json
{
    "Stage": "SST_DECODE_BARCODES",
    "DeblurModes": []
}
```

## Available Parameters

### Stage

The name of the current stage, whose value is a fixed value: `ST_BARCODE_DECODING`.

### DeblurModes

Parameter [`DeblurModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html) defines the mode and priority for deblurring. 
