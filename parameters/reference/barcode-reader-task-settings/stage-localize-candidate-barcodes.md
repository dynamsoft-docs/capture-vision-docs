---
layout: default-layout
title: LocalizeCandidateBarcodesStage - Dynamsoft Barcode Reader Parameters
description: This page defines LocalizeCandidateBarcodesStage object under the BarcodeLocalizationSection.
keywords: LocalizeCandidateBarcodesStage
---

# LocalizeCandidateBarcodesStage

The `LocalizeCandidateBarcodesStage` defines the stage that detects and marks potential barcode locations within the image for further processing.

## Example

```json
{
    "Stage": "SST_LOCALIZE_CANDIDATE_BARCODES",
    "LocalizationModes": []
}
```

## Available Parameters

### Stage

The name of the current stage, whose value is a fixed value: `SST_LOCALIZE_CANDIDATE_BARCODES`.

### LocalizationModes

Parameter [`LocalizationModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/localization-modes.html) controls how to localize barcodes. 
