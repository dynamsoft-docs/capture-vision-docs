---
layout: default-layout
title: Enhance Image Stage - Dynamsoft Document Normalizer Parameters
description: The parameter defines Enhance Image Stage under the Image Enhancement Section.
keywords: Enhance Image Stage
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Enhance Image Stage

The `Enhance Image Stage` is designed at the stage level to adjust the image quality, such as changing the brightness, contrast, and the color mode of the image.

```json
{
    "Stage": "SST_ENHANCE_IMAGE",
	"ColourMode": "ICM_COLOUR",
	"Brightness": 0,
	"Contrast": 0
}
```

## Stage

The stage is named `SST_ENHANCE_IMAGE`.

## ColourMode

Parameter [`ColourMode`](./colour-mode.md) defines the output colour mode of the target image.

## Brightness

Parameter [`Brightness`](./brightness.md) defines the brightness of the target image.

## Contrast

Parameter [`Contrast`](./contrast.md) specifies the contrast of the target image.