---
layout: default-layout
Title: Timeout - Dynamsoft Capture Vision Parameters
Description: The parameter Timeout defines the maximum amount of time (in milliseconds) that the recognition tasks should take per page.
Keywords: timeout, CaptureVisionTemplate
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/capture-vision-template/timeout.html
---

# Timeout

Defines the maximum amount of time (in milliseconds) that should be spent processing each image or frame. It does not include the time taken to load/decode an image from disk into memory.

## Example

```json
{
    "Timeout":10000
}
```

## Parameter Summary

| Timeout Parameter Summary |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br>10000 |
| **Remarks**<br>0: no limitation on the time cost.|
