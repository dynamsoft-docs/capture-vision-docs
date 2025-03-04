---
layout: default-layout
title: ResistDeformationStage - Dynamsoft Barcode Reader Parameters
description: This page defines ResistDeformationStage object under the BarcodeDecodingSection.
keywords: ResistDeformationStage
---

# ResistDeformationStage

The `ResistDeformationStage` defines the stage that applies preprocessing techniques to reduce image deformation and improve barcode recognition accuracy.

## Example

```json
{
    "Stage": "SST_RESIST_DEFORMATION",
    "DeformationResistingModes": []
}
```

## Available Parameters

### Stage

The name of the current stage, whose value is a fixed value: `SST_RESIST_DEFORMATION`.

### DeformationResistingModes

Parameter [`DeformationResistingModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deformation-resisting-modes.html) defines how to handle distorted and deformed barcodes. 
