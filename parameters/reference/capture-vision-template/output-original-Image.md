---
layout: default-layout
Title: OutputOriginalImage - Dynamsoft Capture Vision Parameters
Description: The parameter OutputOriginalImage indicates whether DCV finally outputs the original input image.
Keywords: original image, captured results, CaptureVisionTemplate
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/capture-vision-template/output-raw-Image.html
---

# OutputOriginalImage

Parameter `OutputOriginalImage` indicates whether DCV finally outputs the original input image.

## Example

```json
{
    "OutputOriginalImage":0
}
```

## Parameter Summary

| OutputOriginalImage Parameter Summary |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>0,1 |
| **Default Value**<br>0 |
| **Remarks**<br>0: The original image is not included in the final captured results.<br>1:  The original image is included in the final captured results.|
