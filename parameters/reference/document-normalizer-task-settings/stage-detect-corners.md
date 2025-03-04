---
layout: default-layout
title: Detect Corners Stage - Dynamsoft Document Normalizer Parameters
description: The parameter defines Detect Corners Stage under the Document Detection Section.
keywords: Detect Corners Stage
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Detect Corners Stage

The `Detect Corners Stage` is designed at the stage level to detect corners of quadrilaterals that meet the specified conditions.

```json
{
    "Stage": "SST_DETECT_CORNERS",
	"CornerAngleRange": {
		"MaxValue": 110,
		"MinValue": 70
	}
}
```

## Stage

The stage is named `SST_DETECT_CORNERS`.

## CornerAngleRange

Parameter [`CornerAngleRange`](./corner-angle-range.md) specifies the range of angles (in degrees) of the extracted corners. The corners refer to the corners of a quad or document.