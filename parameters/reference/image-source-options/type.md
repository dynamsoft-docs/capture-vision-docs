---
layout: default-layout
Title: Type - Dynamsoft Capture Vision Parameters
Description: The parameter Type of Dynamsoft Capture Vision defines .
Keywords: Type, ISA
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/image-source-options/type.html
---

# Type

Parameter `Type` indicates the type of the ImageSource object, which helps CVR create the correct type of image source.

## Example

```json
{
    "Type": "IST_DIRECTORY_FETCHER"
}
```

## Parameter Summary

| Type Parameter Summary |
| :--------------------- |
| **Description**<br>Define the type of ImageSource. |
| **Type**<br>*String* |
| **Value range**<br>One of the ImageSourceType as a string.<br>IST_DIRECTORY_FETCHER<br>IST_CAMERA_ENHANCER<br>IST_SCANNER_CONNECTOR |
