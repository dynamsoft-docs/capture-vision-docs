---
layout: default-layout
title: ComplementBarcodeStage - Dynamsoft Barcode Reader Parameters
description: This page defines ComplementBarcodeStage object under the BarcodeDecodingSection.
keywords: ComplementBarcodeStage
---

# ComplementBarcodeStage

The `ComplementBarcodeStage` is designed at the stage level to define the configuration settings for the barcode complement process.

## Example

```json
{
    "Stage": "SST_COMPLEMENT_BARCODE",
    "BarcodeComplementModes": []
}
```

## Available Parameters

### Stage

The name of the current stage, whose value is a fixed value: `SST_COMPLEMENT_BARCODE`.

### BarcodeComplementModes

Parameter [`BarcodeComplementModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/barcode-complement-modes.html) defines how to complement the missing parts of a barcode. 
