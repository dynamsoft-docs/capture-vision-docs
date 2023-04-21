---
layout: default-layout
title: ResourcesPath - Dynamsoft Capture Vision Parameter Reference
description: The parameter ResourcesPath of Dynamsoft Capture Vision. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /parameters/reference/code-parser-task-settings/resources-path.html
---

# ResourcesPath

`ResourcesPath` specifies the directory path that contains the resources needed for code parsing.

## Example

```json
{
    "ResourcesPath" : "../VIN/"
}
```

## Parameter Summary

| Brightness Parameter Summary |
| :------------- |
| **Type**<br>*String* |
| **Range**<br>any valid string |
| **Default Value**<br>"" |

**Remarks**

- The default value, "", means the resources directory under current executable path.
- `ResourcesPath` can be either an absolute path or a relative path. When the value is a relative path, it's relative to current executable path.
