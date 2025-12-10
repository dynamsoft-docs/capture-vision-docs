---
layout: default-layout
title: OutputRawImage - Dynamsoft Capture Vision Parameters
description: The parameter OutputRawImage indicates whether DCV finally outputs the original input image.
keywords: raw image, captured results, CaptureVisionTemplate
permalink: /parameters/reference/capture-vision-template/output-raw-image.html
---
# OutputRawImage

Parameter `OutputRawImage` indicates whether DCV finally outputs the original input image.

## JSON Structure

**Location in template:**
```
CaptureVisionTemplates[i]
    └── OutputRawImage
```

**Parent object:** [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object

**Example:**

```json
{
    "OutputRawImage": 0
}
```

> [!NOTE]
> - This snippet shows only the `OutputRawImage` parameter.
> - To use it, embed this parameter within a [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| OutputRawImage Parameter Details |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>0,1 |
| **Default Value**<br>0 |
| **Remarks**<br>0: The raw image is not included in the final captured results.<br>1: The raw image is included in the final captured results.|
