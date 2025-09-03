---
layout: default-layout
title: CodeSpecifications - Dynamsoft Capture Vision Parameter Reference
description: The parameter CodeSpecifications of Dynamsoft Capture Vision. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /parameters/reference/code-parser-task-settings/code-specifications.html
---

# CodeSpecifications

Parameter `CodeSpecifications` specifies the names of CodeSpecification used for code parsing.

## Example

```json
{
    "CodeSpecifications" : ["VIN"]
}
```

## Parameter Summary

| Brightness Parameter Summary |
| :------------- |
| **Type**<br>*string array* |
| **Range**<br>Any valid string |
| **Default Value**<br>[] |

**Remarks**

- The default value, [], means all CodeSpecification under resources path will be used.
- A `CodeSpecification` is a file named as [Name].dcpres which defines the fields and parsing rules for a specific code type.
