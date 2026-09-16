---
layout: default-layout
title: Name - Dynamsoft Label Recognizer LabelRecognizerTaskSetting Parameters
description: The parameter Name defines the unique identifier of a LabelRecognizerTaskSetting object.
keywords: top-level object, name, unique identifier
---

# Name

`Name` represents the name of a `LabelRecognizerTaskSetting` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── Name
```

**Parent object:** [LabelRecognizerTaskSetting]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/index.html)

**Example:**

```json
{
    "Name": "lr_0"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within a [LabelRecognizerTaskSetting]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/index.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters_reference }}index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters_reference }}index.html#minimal-valid-json-example)

## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |
