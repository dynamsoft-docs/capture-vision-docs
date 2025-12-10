---
layout: default-layout
title: FileFilter - Dynamsoft Capture Vision Parameters
description: The parameter FileFilter of Dynamsoft Capture Vision defines .
keywords: File filter, ISA
---

# FileFilter

Parameter `FileFilter` specifies a file name filter string, which determines which files are fetched.

## JSON Structure

**Location in template:**
```
ImageSourceOptions
    └── FileFilter
```

**Parent object:** [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object

**Example:**

```json
{
    "FileFilter": "*.JPG"
}
```

> [!NOTE]
> - This snippet shows only the `FileFilter` parameter.
> - To use it, embed this parameter within a [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| FileFilter Parameter Details |
| :----------------------------------- |
| **Description**<br>A file name filter string |
| **Type**<br>*String* |
| **Value range**<br>One of the files extension name. For example: "\*.BMP;\*.JPG;\*.GIF", or "\*.\*", etc. |
| **Default Value**<br>"" |
