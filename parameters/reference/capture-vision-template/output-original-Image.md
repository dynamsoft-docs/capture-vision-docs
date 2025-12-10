---
layout: default-layout
title: OutputOriginalImage - Dynamsoft Capture Vision Parameters
description: The parameter OutputOriginalImage indicates whether DCV finally outputs the original input image.
keywords: original image, captured results, CaptureVisionTemplate
permalink: /parameters/reference/capture-vision-template/output-original-image.html
---
# OutputOriginalImage

Parameter `OutputOriginalImage` indicates whether DCV finally outputs the original input image.

## JSON Structure

**Location in template:**
```
CaptureVisionTemplates[i]
    └── OutputOriginalImage
```

**Parent object:** [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object

**Example:**

```json
{
    "OutputOriginalImage":0
}
```

> [!NOTE]
> - This snippet shows only the `OutputOriginalImage` parameter.
> - To use it, embed this parameter within a [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| OutputOriginalImage Parameter Details |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>0,1 |
| **Default Value**<br>0 |
| **Remarks**<br>0: The original image is not included in the final captured results.<br>1:  The original image is included in the final captured results.|
