---
layout: default-layout
title: ImageSourceName - Dynamsoft Capture Vision Parameters
description: The parameter ImageSourceName of Dynamsoft Capture Vision defines the name of the ImageSource object.
keywords: image source, CaptureVisionTemplate
permalink: /parameters/reference/capture-vision-template/image-source-name.html
---
# ImageSourceName

Parameter `ImageSourceName` indicates the input source name, used to refer to the `ImageSource` object. It is used to define the input image source of DCV.

## JSON Structure

**Location in template:**
```
CaptureVisionTemplates[i]
    └── ImageSourceName
```

**Parent object:** [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object

**Example:**

```json
{
    "ImageSourceName": "isa_1"
}
```

> [!NOTE]
> - This snippet shows only the `ImageSourceName` parameter.
> - To use it, embed this parameter within a [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| ImageSourceName Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of the `ImageSource` object. |
| **Default Value**<br>"" |
| **Remarks**<br>"" indicates that there is no default input image source, which needs to be specified using the `SetInput` API.|
