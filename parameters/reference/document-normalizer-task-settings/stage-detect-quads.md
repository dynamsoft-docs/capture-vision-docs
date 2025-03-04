---
layout: default-layout
title: Detect Quads Stage - Dynamsoft Document Normalizer Parameters
description: The parameter defines Detect Quads Stage under the Document Detection Section.
keywords: Detect Quads Stage
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Detect Quads Stage

The `Detect Quads Stage` is designed at the stage level to detect complete quadrilaterals.

```json
{
"Stage": "SST_DETECT_QUADS",
"QuadrilateralDetectionModes": [
	{
		"Mode": "QDM_GENERAL"
	}
]
}
```

## Stage

The stage is named `SST_DETECT_QUADS`.

## QuadrilateralDetectionModes

Parameter [`QuadrilateralDetectionModes`](./quadrilateral-detection-modes.md) controls the quadrilateral detection process on an image.