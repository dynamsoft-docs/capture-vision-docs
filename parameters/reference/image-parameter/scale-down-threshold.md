---
layout: default-layout
title: ScaleDownThreshold - Dynamsoft Capture Vision Parameters
description: The parameter ScaleDownThreshold of Dynamsoft Capture Vision is for defining the threshold for image shrinking.
keywords: ScaleDownThreshold, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /parameters/reference/image-parameter/scale-down-threshold.html
---


# ScaleDownThreshold

Parameter `ScaleDownThreshold` defines the threshold for image shrinking.

## Example

```json
{
    "ScaleDownThreshold": 1024
}
```

## Parameter Summary

When the input image is too large, this parameter ScaleDownThreshold can be used to reduce the size.

| ScaleDownThreshold Parameter Summary |
| :---------------------------------- |
| **Description**<br>If the shorter edge size is larger than the given value, the library will calculate the required height and width of the barcode image and shrink the image to that size before going to further processes. Otherwise, it will perform processes on the original image. |
| **Type**<br>*int* |
| **Value range**<br>[512, 0x7fffffff] |
| **Default Value**<br>2300 |
