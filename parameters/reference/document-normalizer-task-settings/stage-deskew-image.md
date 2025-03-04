---
layout: default-layout
title: Deskew Image Stage - Dynamsoft Document Normalizer Parameters
description: The parameter defines Deskew Image Stage under the Document Deskewing Section.
keywords: Deskew Image Stage
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Deskew Image Stage

The `Deskew Image Stage` is designed at the stage level to de-skew the quadrilateral to transform it into a rectangle.

```json
{
	"Stage": "SST_DESKEW_IMAGE",
	"DeskewMode": {
		"ContentDirection": 0,
		"Mode": "DSM_PERSPECTIVE_CORRECTION"
	},
	"PageSize": [
		-1,
		-1
	]
}
```

## Stage

The stage is named `SST_DESKEW_IMAGE`.

## DeskewMode

Parameter [`DeskewMode`](./deskew-mode.md) specifies the method in which the deskew process way used to apply the deskew process on the target image.

## PageSize

Parameter [`PageSize`](./page-size.md) sets the page size (width by height in pixels) of the image after deskew process.