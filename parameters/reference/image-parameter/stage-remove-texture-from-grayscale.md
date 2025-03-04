---
layout: default-layout
title: Remove Texture from Grayscale Stage Parameters - Dynamsoft Capture Vision Parameters
description: The parameters that available under remove texture from grayscale stage of Dynamsoft Capture Vision.
keywords: Stages, remove texture from grayscale
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Remove Texture from Grayscale Stage Parameters

The parameters that available under the remove texture from grayscale stage.

```json
{
    "Stage":"SST_REMOVE_TEXTURE_FROM_GRAYSCALE",
    "TextureRemovalStrength": 2
},
```

## Stage

The stage name of remove texture from grayscale stage is `SST_REMOVE_TEXTURE_FROM_GRAYSCALE`.

## TextureRemovalStrength

Defines how to remove texture from grayscale.

| TextureRemovalStrength Parameter Summary |
| :---------------------------------- |
| **Type**<br>*int* |
| **Value range**<br>[1,9] |
| **Default Value**<br>2 for BarcodeReaderTask & DocumentNormalizerTask<br>1 for LabelRecognizerTask |
