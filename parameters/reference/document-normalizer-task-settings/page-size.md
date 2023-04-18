---
layout: default-layout
Title: PageSize - Dynamsoft Document Normalizer Parameters
Description: The parameter PageSize of Dynamsoft Document Normalizer is XXX.
Keywords: Page size
needAutoGenerateSidebar: true
noTitleIndex: true
---

# PageSize

Sets the page size (width by height in pixels) of the normalized image.

```json
{
    "PageSize" : [ 210, 297 ]
}
```

| PageSize Parameter Details |
| :--------------- |
| **Type**<br><i>int[2]</i> |
| **Range**<br>Each member should be a int value betweem [-1,0x7fffffff]. |
| **Default Value**<br>[-1,-1] |
| **Remarks**<br><li>A page size is defined as: [TargetPageWidth, TargetPageHeight].<li>TargetPageWidth * TargetPageHeight < 100000000.<li>If any of TargetPageWidth and TargetPageHeight is 0 or -1, the original width and height of the detected content will be used. |