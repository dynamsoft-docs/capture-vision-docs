---
layout: default-layout
title: Recursive - Dynamsoft Capture Vision Parameters
description: The parameter Recursive of Dynamsoft Capture Vision defines .
keywords: Recursive, ISA
permalink: /parameters/reference/image-source-options/recursive.html
---
# Recursive

Parameter `Recursive` indicates whether to fetch files recursively.

## JSON Structure

**Location in template:**
```
ImageSourceOptions
    └── Recursive
```

**Parent object:** [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object

**Example:**

```json
{
    "Recursive": 1
}
```

> [!NOTE]
> - This snippet shows only the `Recursive` parameter.
> - To use it, embed this parameter within a [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Recursive Parameter Details |
| :-------------------------- |
| **Description**<br>Use 0 (false) and 1 (true) to define whether to fetch files. |
| **Type**<br>*int* |
| **Value range**<br>[0,1] |
| **Default Value**<br>1 |
