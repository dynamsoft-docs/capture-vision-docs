---
layout: default-layout
title: Binarize Image Stage Parameters - Dynamsoft Capture Vision Parameters
description: The parameters that available under binarize image stage of Dynamsoft Capture Vision.
keywords: Stages, binarize image, binarization modes, BinarizationMode
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Binarize Image Stage Parameters

The parameters that available under the Binarize Image Stage.

```json
{
    "Stage":"SST_BINARIZE_IMAGE",
    "BinarizationModes" : []
}
```

## Stage

The stage name of binarize image stage is `SST_BINARIZE_IMAGE`.

## BinarizationModes

Defines the binarization options with an array of [`BinarizationMode`](binarization-modes.md) objects. The modes in the array will be executed sequentially until the task is completed.

| Stage Parameter Summary |
| :---------------------- |
| **Type**<br>An array of [`BinarizationMode`](binarization-modes.md) objects |
