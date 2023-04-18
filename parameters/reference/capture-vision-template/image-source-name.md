---
layout: default-layout
Title: ImageSourceName - Dynamsoft Capture Vision Parameters
Description: The parameter ImageSourceName of Dynamsoft Capture Vision defines the name of the ImageSource object.
Keywords: image source, CaptureVisionTemplate
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceName

Indicates the input source name, used to refer to the `ImageSource` object. It is used to define the input image source of DCV.

```json
{
    "ImageSourceName": "isa_1"
}
```

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of the `ImageSource` object. |
| **Default Value**<br>"" |
| **Remarks**<br>"" indicates that there is no default input image source, which needs to be specified using the `SetInput` API.|