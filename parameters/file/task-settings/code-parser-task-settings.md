---
layout: default-layout
title: CodeParserTaskSetting - Dynamsoft Capture Vision Parameter File
description: The CodeParserTaskSetting object in the Dynamsoft Capture Vision Parameter File. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /parameters/file/task-settings/code-parser-task-setting.html
---

# CodeParserTaskSetting Object

## Parameter Organization

A `CodeParserTaskSetting` object is defined as below:

| Key Name | Value Type | Required or Optional | Description |
|---|---|---|---|
| Name | string | Mandatory | Sets the name of current `CodeParserTaskSetting` object. The value must be unique between all `task-setting` objects. |
| CodeSpecifications | string array | Optional | Sets the value for parameter [CodeSpecifications]({{site.parameterReference}}code-specifications.html) to define an array of specification file name objects that determine how to parse the code string |
| ResourcesPath | string | Optional | Sets the value for parameter [ResourcesPath]({{site.parameterReference}}resources-path.html) to define the directory path that contains the resources needed for the code parser. |

Here is a sample:

```JSON
{
    "Name": "CPT1_PARSE_VIN",
    "CodeSpecifications": ["VIN"], 
    "ResourcesPath": "../VIN/" 
}
```
