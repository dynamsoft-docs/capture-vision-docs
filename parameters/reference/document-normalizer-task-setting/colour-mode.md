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

Colour Mode List

- ICM_BINARY
- ICM_GRAYSCALE
- ICM_COLOUR

| ColourMode Parameter Details |
| :--------------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the colour mode as a string. |
| **Default Value**<br>"ICM_BINARY" |
