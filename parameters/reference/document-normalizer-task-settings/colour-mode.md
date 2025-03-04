---
layout: default-layout
title: ColourMode - Dynamsoft Document Normalizer Parameters
description: The parameter ColourMode of Dynamsoft Document Normalizer defines the output colour mode of the image.
keywords:
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# ColourMode

Parameter `ColourMode` defines the output colour mode of the target image. It influence the image that output by both `CapturedResult` and `IntermediateResult`.

## Example

```json
{
    "ColourMode": "ICM_GRAYSCALE"
}
```

## Parameter Summary

| ColourMode Parameter Summary |
| :--------------------------- |
| **Type**<br>*String* |
| **Available Colour Mode List**<br><br>ICM_BINARY<br>ICM_GRAYSCALE<br>ICM_COLOUR |
| **Default Value**<br>"ICM_COLOUR" |
