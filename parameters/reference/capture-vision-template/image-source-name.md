---
layout: default-layout
title: ImageSourceName - Dynamsoft Capture Vision Parameters
description: The parameter ImageSourceName of Dynamsoft Capture Vision defines the name of the ImageSource object.
keywords: image source, CaptureVisionTemplate
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/capture-vision-template/image-source-name.html
---

# ImageSourceName

Parameter `ImageSourceName` indicates the input source name, used to refer to the `ImageSource` object. It is used to define the input image source of DCV.

## Example

```json
{
    "ImageSourceName": "isa_1"
}
```

## Parameter Summary

| ImageSourceName Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of the `ImageSource` object. |
| **Default Value**<br>"" |
| **Remarks**<br>"" indicates that there is no default input image source, which needs to be specified using the `SetInput` API.|
