---
layout: default-layout
Title: LineExtractionModes - Dynamsoft Document Normalizer Parameters
Description: The parameter LineExtractionModes of Dynamsoft Document Normalizer is XXX.
Keywords:
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LineExtractionModes

`LineExtractionModes` specifies the algorithm used to extract lines. It currently consist of `LEM_GENERAL` and `LEM_MARGIN_BASED`. Each mode representing a different way to extract lines.

```json
{
    "LineExtractionModes":
    [
        {
            "Mode": "LEM_GENERAL"
        },
        {
            "Mode": "LEM_MARGIN_BASED" 
        }
    ]
}
```

LineExtractionModes is defined with an array of mode objects. Each array members can be an object of either `LEM_GENERAL` or `LEM_MARGIN_BASED`.

| LineExtractionModes Parameter Details |
| :----------------------- |
| **Type**<br> |
| **Range**<br> |
| **Default Value**<br> |
