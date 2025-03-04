---
layout: default-layout
title: ScaleBarcodeImageStage - Dynamsoft Barcode Reader Parameters
description: This page defines ScaleBarcodeImageStage object under the BarcodeDecodingSection.
keywords: ScaleBarcodeImageStage
---

# ScaleBarcodeImageStage

The `ScaleBarcodeImageStage` defines the stage where the barcode image is scaled according to the specified scaling mode to optimize recognition.

## Example

```json
{
    "Stage": "SST_SCALE_BARCODE_IMAGE",
    "BarcodeScaleModes": []
}
```

## Available Parameters

### Stage

The name of the current stage, whose value is a fixed value: `SST_SCALE_BARCODE_IMAGE`.

### BarcodeScaleModes

Parameter [`BarcodeScaleModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/barcode-scale-modes.html) defines the scaling mode applied during barcode recognition. 
