---
layout: default-layout
title: Name - Dynamsoft Capture Vision Parameter Reference CodeParserTaskSetting Object.
description: The parameter Name defines the unique identifier of CodeParserTaskSetting object.
keywords: top-level object, name, unique identifier
permalink: /parameters/reference/code-parser-task-settings/name.html
---
# Name

Parameter `Name` represents the name of a `CodeParserTaskSetting` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
CodeParserTaskSettingOptions[i]
    └── Name
```

**Parent object:** [CodeParserTaskSetting]({{ site.dcvb_parameters }}file/task-settings/code-parser-task-settings.html) object

**Example:**

```json
{
    "Name" : "cp_0"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within a [CodeParserTaskSetting]({{ site.dcvb_parameters }}file/task-settings/code-parser-task-settings.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |
