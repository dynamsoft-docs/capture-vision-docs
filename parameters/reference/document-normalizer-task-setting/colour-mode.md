---
layout: default-layout
Title: ColourMode - Dynamsoft Document Normalizer Parameters
Description: The parameter ColourMode of Dynamsoft Document Normalizer defines the output colour mode of the normalized image.
Keywords:
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ColourMode

Parameter `ColourMode` defines the output colour mode of the normalized image. It influence the normalized image that output by both `CapturedResult` and `IntermediateResult`.

```json
{
    "ColourMode": "ICM_GRAYSCALE"
}
```

| ColourMode Parameter Details |
| :--------------------------- |
| **Type**<br>*String* |
| Range<br>"ICM_BINARY", "ICM_GRAYSCALE" or "ICM_COLOUR". |
| Default Value<br>`"ICM_BINARY"` |
