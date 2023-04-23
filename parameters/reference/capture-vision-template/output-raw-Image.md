---
layout: default-layout
Title: OutputRawImage - Dynamsoft Capture Vision Parameters
Description: The parameter OutputRawImage indicates whether DCV finally outputs the original input image.
Keywords: raw image, captured results, CaptureVisionTemplate
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/capture-vision-template/output-raw-Image.html
---

# OutputRawImage

Parameter `OutputRawImage` indicates whether DCV finally outputs the original input image.

## Example

```json
{
    "OutputRawImage":0
}
```

## Parameter Summary

| OutputRawImage Parameter Summary |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>0,1 |
| **Default Value**<br>0 |
| **Remarks**<br>0: The raw image is not included in the final captured results.<br>1:  The raw image is included in the final captured results.|
