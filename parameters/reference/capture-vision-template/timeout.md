---
layout: default-layout
title: Timeout - Dynamsoft Capture Vision Parameters
description: The parameter Timeout defines the maximum amount of time (in milliseconds) that the recognition tasks should take per page.
keywords: timeout, CaptureVisionTemplate
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/capture-vision-template/timeout.html
---

# Timeout

Parameter `Timeout` defines the maximum amount of time (in milliseconds) that should be spent processing each image or frame. It does not include the time taken to load/decode an image from disk into memory.

The timer starts when the library start processing the first task of the image. You may still receive processing results even if it times out:

* If a part of the tasks are finished, the results of the finished tasks are output. You will receive an `EC_TIMEOUT` error code in your `CapturedResult` as well.
* If all tasks are not finished:
  * If there exist results of the unfinished tasks, the existing results are output. You will receive an `EC_TIMEOUT` error code in your `CapturedResult` as well.
  * If none of the tasks has result, you still receive a CapturedResult with an empty array of `CapturedResultItem` and the error code `EC_TIMEOUT`.

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
