---
layout: default-layout
title: Type - Dynamsoft Capture Vision Parameters
description: The parameter Type of Dynamsoft Capture Vision defines .
keywords: Type, ISA
permalink: /parameters/reference/image-source-options/type.html
---
# Type

Parameter `Type` indicates the type of the ImageSource object, which helps CVR create the correct type of image source.

## JSON Structure

**Location in template:**
```
ImageSourceOptions
    └── Type
```

**Parent object:** [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object

**Example:**

```json
{
    "Type": "IST_DIRECTORY_FETCHER"
}
```

> [!NOTE]
> - This snippet shows only the `Type` parameter.
> - To use it, embed this parameter within a [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Type Parameter Details |
| :--------------------- |
| **Description**<br>Define the type of ImageSource. |
| **Type**<br>*String* |
| **Value range**<br>One of the ImageSourceType as a string.<br>IST_DIRECTORY_FETCHER<br>IST_CAMERA_ENHANCER<br>IST_SCANNER_CONNECTOR |
