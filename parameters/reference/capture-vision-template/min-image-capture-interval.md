---
layout: default-layout
title: MinImageCaptureInterval - Dynamsoft Capture Vision Parameters
description: The parameter MinImageCaptureInterval defines the minimum time interval (in milliseconds) allowed between consecutive image captures.
keywords: MinImageCaptureInterval, CaptureVisionTemplate
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# MinImageCaptureInterval

Parameter `MinImageCaptureInterval` defines the minimum time interval (in milliseconds) allowed between consecutive image captures.

## Example

```json
{
    "MinImageCaptureInterval":100
}
```

## Parameter Summary

| MinImageCaptureInterval Parameter Summary |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br>0 |
| **Remarks**<br>This property represents the minimum time interval (in milliseconds) that must elapse before the next image capture operation can be initiated.
Setting a larger value for this property will introduce a delay between image captures, while setting a smaller value allows for more frequent captures. It can be used to reduce the computational frequency, which can effectively lower energy consumption. Please note that the actual time interval between captures may be longer than the specified minimum interval due to various factors, such as image processing time and hardware limitations.|
