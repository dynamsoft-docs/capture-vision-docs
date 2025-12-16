---
layout: default-layout
title: BaseLabelRecognizerTaskSettingName - Dynamsoft Label Recognizer Parameters
description: The parameter BaseLabelRecognizerTaskSettingName defines the name of the inherited LabelRecognizerTaskSetting object.
keywords: inheritance, LabelRecognizerTaskSetting
---

# BaseLabelRecognizerTaskSettingName

`BaseLabelRecognizerTaskSettingName` represents the name of another `LabelRecognizerTaskSetting` object. It is used to inherit the parameters defined in its parent `LabelRecognizerTaskSetting` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── BaseLabelRecognizerTaskSettingName
```

**Parent object:** [LabelRecognizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/label-recognizer-task-settings.html)

**Example:**

```json
{
    "BaseLabelRecognizerTaskSettingName": "dlr_task_1"
}
```

> [!NOTE]
> - This snippet shows only the `BaseLabelRecognizerTaskSettingName` parameter.
> - To use it, embed this parameter within a [LabelRecognizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/label-recognizer-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| BaseLabelRecognizerTaskSettingName Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of the inherited `LabelRecognizerTaskSetting` object. |
| **Default Value**<br>"" |
| **Remarks**<br>(1) "" stands for no inheritance.<br>(2) If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.|
