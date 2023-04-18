---
layout: default-layout
title: CodeSpecifications - Dynamsoft Capture Vision Parameter Reference
description: The parameter CodeSpecifications of Dynamsoft Capture Vision. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /parameters/reference/code-specifications.html
---

# CodeSpecifications

`CodeSpecifications` specifies the names of CodeSpecification used for code parsing.

```json
{
    "CodeSpecifications" : ["VIN"]
}
```

| Brightness Parameter Summary |
| :------------- |
| **Type**<br>*string array* |
| **Range**<br>any valid string |
| **Default Value**<br>[], which means all CodeSpecification under resources path will be used. |

**Remarks**

A `CodeSpecification` is a file named as [Name].dcpres which defines the fields and parsing rules for a specific code type.
