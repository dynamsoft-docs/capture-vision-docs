---
layout: default-layout
title: PageSize - Dynamsoft Document Normalizer Parameters
description: The parameter PageSize of Dynamsoft Document Normalizer is XXX.
keywords: Page size
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# PageSize

Parameter `PageSize` sets the page size (width by height in pixels) of the target image.

## Example

```json
{
    "PageSize" : [ 210, 297 ]
}
```

## Parameter Summary

| PageSize Parameter Summary |
| :--------------- |
| **Type**<br><i>int[2]</i> |
| **Range**<br>Each member should be a int value betweem [-1,0x7fffffff]. |
| **Default Value**<br>[-1,-1] |
| **Remarks**<br>A page size is defined as: [TargetPageWidth, TargetPageHeight].<br>TargetPageWidth * TargetPageHeight < 100000000.<br>If any of TargetPageWidth and TargetPageHeight is 0 or -1, the original width and height of the detected content will be used. |
