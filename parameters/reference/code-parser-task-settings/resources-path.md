---
layout: default-layout
title: ResourcesPath - Dynamsoft Capture Vision Parameter Reference
description: The parameter ResourcesPath of Dynamsoft Capture Vision. 
permalink: /parameters/reference/code-parser-task-settings/resources-path.html
---
# ResourcesPath

Parameter `ResourcesPath` specifies the directory path that contains the resources needed for code parsing.

## JSON Structure

**Location in template:**
```
CodeParserTaskSettingOptions[i]
    └── ResourcesPath
```

**Parent object:** [CodeParserTaskSetting]({{ site.dcvb_parameters }}file/task-settings/code-parser-task-settings.html) object

**Example:**

```json
{
    "ResourcesPath" : "../VIN/"
}
```

> [!NOTE]
> - This snippet shows only the `ResourcesPath` parameter.
> - To use it, embed this parameter within a [CodeParserTaskSetting]({{ site.dcvb_parameters }}file/task-settings/code-parser-task-settings.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Brightness Parameter Details |
| :------------- |
| **Type**<br>*String* |
| **Range**<br>any valid string |
| **Default Value**<br>"" |

**Remarks**

- The default value, "", means the resources directory under current executable path.
- `ResourcesPath` can be either an absolute path or a relative path. When the value is a relative path, it's relative to current executable path.
