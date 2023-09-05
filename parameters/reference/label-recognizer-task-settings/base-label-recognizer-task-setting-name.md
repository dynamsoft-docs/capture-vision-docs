---
layout: default-layout
title: BaseLabelRecognizerTaskSettingName - Dynamsoft Label Recognizer Parameters
description: The parameter BaseLabelRecognizerTaskSettingName of Dynamsoft Label Recognizer defines the name of the inherited LabelRecognizerTaskSetting object.
keywords: inheritance, LabelRecognizerTaskSetting
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/label-recognizer-task-settings/base-label-recognizer-task-setting-name.html
---

# BaseLabelRecognizerTaskSettingName

Parameter `BaseLabelRecognizerTaskSettingName` represents the name of another `LabelRecognizerTaskSetting` object. It is used to inherit the parameters defined in its parent `LabelRecognizerTaskSetting` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## Example

```json
{
    "BaseLabelRecognizerTaskSettingName": "dlr_task_1"
}
```

## Parameter Summary

| BaseLabelRecognizerTaskSettingName Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of the inherited `LabelRecognizerTaskSetting` object. |
| **Default Value**<br>"" |
| **Remarks**<br>(1) "" stands for no inheritance.<br>(2) If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.|
