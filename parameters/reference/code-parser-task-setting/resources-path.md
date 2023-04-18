---
layout: default-layout
title: ResourcesPath - Dynamsoft Capture Vision Parameter Reference
description: The parameter ResourcesPath of Dynamsoft Capture Vision. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /parameters/reference/resources-path.html
---

# ResourcesPath

`ResourcesPath` specifies the directory path that contains the resources needed for code parsing.

```json
{
    "ResourcesPath" : "../VIN/"
}
```

| Brightness Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>any valid string |
| **Default Value**<br>"", which means the resources directory under current executable path. |

**Remarks**

`ResourcesPath` can be either an absolute path or a relative path. When the value is a relative path, it's relative to current executable path.
