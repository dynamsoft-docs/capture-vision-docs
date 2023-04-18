---
layout: default-layout
Title: TaskSettingNameArray - Dynamsoft Capture Vision Parameters
Description: The parameter TaskSettingNameArray of Dynamsoft Capture Vision defines the collection of image ROI processing object names.
Keywords: task settings, TargetROIDef
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TaskSettingNameArray

Represents the collection of task setting object names, used to refer to the [`BarcodeReaderTaskSetting`](../../file/task-settings/barcode-reader-task-settings.md),[`LabelRecognizerTaskSetting`](../../file/task-settings/label-recognizer-task-settings.md),[`DocumentNormalizerTaskSetting`](../../file/task-settings/document-normalizer-task-settings.md) objects. It is used to define recognition tasks such as reading barcodes, recognizing labels, or detecting document quads.

```json
{
    "TaskSettingNameArray": ["dbr_task", "dlr_task", "ddn_task"]
}
```

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element represents the name of a `BarcodeReaderTaskSetting` object, `LabelRecognizerTaskSetting` object, or `DocumentNormalizerTaskSetting` object. |
| **Default Value**<br>	["dbr_task_default", "dlr_task_default", "ddn_task_default"] |
| **Remarks**<br>If `TaskSettingNameArray` is not specified, a default array ["dbr_task_default", "dlr_task_default", "ddn_task_default"] will be created. The TargetROIDef object will have a default configuration of tasks including one barcode reading task, one label recognition task, and one document normalizer task.|