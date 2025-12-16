---
layout: default-layout
title:  Name - Dynamsoft Capture Vision OutputTaskSetting Object.
description: The parameter Name defines the unique identifier of a OutputTaskSetting object.
keywords: top-level object, name, unique identifier
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/output-task-setting/name.html
---

# Name

Parameter `Name` represents the name of a `OutputTaskSetting` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
OutputTaskSettingOptions[i]
    └── Name
```

**Parent object:** [OutputTaskSetting]({{ site.dcvb_parameters }}file/task-settings/output-task-setting.html) object

**Example:**

```json
{
    "Name" : "output_task"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within a [OutputTaskSetting]({{ site.dcvb_parameters }}file/task-settings/output-task-setting.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |
