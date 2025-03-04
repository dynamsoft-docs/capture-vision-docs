---
layout: default-layout
title: Predetect Regions Stage - Dynamsoft Label Recognizer Parameters
description: The parameter defines Predetect Regions Stage under the Regions Predetection Section.
keywords: Predetect Regions Stage
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Predetect Regions Stage

The `Predetect Regions Stage` is designed at the stage level to identify regions of interest (ROIs). The pre-detected region may be identified based on color features, grayscale features, or neural network localization.

```json
{
    "Stage": "SST_PREDETECT_REGIONS",
    "RegionPredetectionModes": []
}
```

## Stage

The stage is named `SST_PREDETECT_REGIONS`.

## RegionPredetectionModes

Parameter [`RegionPredetectionModes`](../image-parameter/region-predetection-modes.md) controls how to find a region of interest (ROI) within the image or frame. 
