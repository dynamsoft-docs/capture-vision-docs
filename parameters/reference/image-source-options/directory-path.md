---
layout: default-layout
title: DirectoryPath - ImageSource - Dynamsoft Capture Vision Parameters
description: The parameter DirectoryPath defines a path when the library have to read files.
keywords: Directory path
permalink: /parameters/reference/image-source-options/directory-path.html
---
# DirectoryPath

Parameter `DirectoryPath` defines a path when the library have to read files.

## JSON Structure

**Location in template:**
```
ImageSourceOptions
    └── DirectoryPath
```

**Parent object:** [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object

**Example:**

```json
{
    "DirectoryPath" : "D:\\ImageSourceDirectory\\"
}
```

> [!NOTE]
> - This snippet shows only the `DirectoryPath` parameter.
> - To use it, embed this parameter within a [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| DirectoryPath Parameter Details |
| :------------- |
| **Type**<br>*String* |
