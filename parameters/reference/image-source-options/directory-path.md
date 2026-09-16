---
layout: default-layout
title: DirectoryPath - ImageSource - Dynamsoft Capture Vision Parameters
description: Reference for the DirectoryPath parameter in the Dynamsoft Capture Vision ImageSource object, which specifies the local directory path from which image files are fetched for processing.
keywords: Directory path
---
# DirectoryPath

Parameter `DirectoryPath` defines a path when the library have to read files.

## JSON Structure

**Location in template:**
```
ImageSourceOptions
    └── DirectoryPath
```

**Parent object:** [ImageSource]({{ site.dcvb_parameters_reference }}image-source-options/index.html) object

**Example:**

```json
{
    "DirectoryPath" : "D:\\ImageSourceDirectory\\"
}
```

> [!NOTE]
> - This snippet shows only the `DirectoryPath` parameter.
> - To use it, embed this parameter within a [ImageSource]({{ site.dcvb_parameters_reference }}image-source-options/index.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters_reference }}index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters_reference }}index.html#minimal-valid-json-example)

## Parameter Details

| DirectoryPath Parameter Details |
| :------------- |
| **Type**<br>*String* |
