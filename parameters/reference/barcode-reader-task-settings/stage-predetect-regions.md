---
layout: default-layout
title: PredetectRegionsStage - Dynamsoft Barcode Reader Parameters
description: This page defines PredetectRegionsStage object under the Regions Predetection Section.
keywords: PredetectRegionsStage
---

# PredetectRegionsStage

The `PredetectRegionsStage` defines the stage that identifies potential barcode regions before the main detection process.

## Example

```json
{
    "Stage": "SST_PREDETECT_REGIONS",
    "RegionPredetectionModes": []
}
```

## Available Parameters

### Stage

The name of the current stage, whose value is a fixed value: `ST_BARCODE_DECODING`.

### RegionPredetectionModes

Parameter [`RegionPredetectionModes`]({{ site.dcvb_parameters_reference }}image-parameter/region-predetection-modes.html) controls how to find a region of interest (ROI) within the image or frame. 
