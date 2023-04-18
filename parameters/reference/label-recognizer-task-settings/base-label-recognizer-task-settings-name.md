---
layout: default-layout
Title: BaseLabelRecognizerTaskSettingsName - Dynamsoft Label Recognizer Parameters
Description: The parameter BaseLabelRecognizerTaskSettingsName of Dynamsoft Label Recognizer defines the name of the inherited LabelRecognizerTaskSetting object.
Keywords: inheritance, LabelRecognizerTaskSetting
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BaseLabelRecognizerTaskSettingsName

Represents the name of another `LabelRecognizerTaskSetting` object. It is used to inherit the parameters defined in its parent `LabelRecognizerTaskSetting` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

```json
{
    "BaseLabelRecognizerTaskSettingsName": "dlr_task_1"
}
```

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of the inherited `LabelRecognizerTaskSetting` object. |
| **Default Value**<br>"" |
| **Remarks**<br>(1) "" stands for no inheritance.<br>(2) If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.|
