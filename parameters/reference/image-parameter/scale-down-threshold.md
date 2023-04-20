---
layout: default-layout
title: ScaleDownThreshold - Dynamsoft Capture Vision Parameters
description: The parameter ScaleDownThreshold of Dynamsoft Capture Vision is for defining the threshold for image shrinking.
keywords: ScaleDownThreshold, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/image-parameter/scale-down-threshold.html
---


# ScaleDownThreshold

Parameter ScaleDownThreshold defines the threshold for image shrinking.

## Example

```json
{
    "ScaleDownThreshold": 1024
}
```

## Parameter Summary

### Child Parameters

When the input image is too large, this parameter ScaleDownThreshold can be used to reduce the size.

<table style = "text-align:left">
    <tr>
        <th>ScaleDownThreshold Parameter Details</th>
    </tr>
    <tr>
        <td><b>Description</b><br>If the shorter edge size is larger than the given value, the library will calculate the required height and width of the barcode image and shrink the image to that size before going to further processes. Otherwise, it will perform processes on the original image.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Value range</b><br>[512, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>2300
        </td>
    </tr>
</table>

## See Also
- [Capture Vision Template]()
- [Image Parameter]() 