---
layout: default-layout
title: TaskSettingNameArray - Dynamsoft Capture Vision Parameters
description: The parameter TaskSettingNameArray of Dynamsoft Capture Vision defines the collection of image ROI processing object names.
keywords: task settings, TargetROIDef
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/target-roi-def/task-setting-name-array.html
---

# TaskSettingNameArray

Parameter `TaskSettingNameArray` represents the collection of task setting object names, used to refer to the [`BarcodeReaderTaskSetting`](../../file/task-settings/barcode-reader-task-settings.md),[`LabelRecognizerTaskSetting`](../../file/task-settings/label-recognizer-task-settings.md),[`DocumentNormalizerTaskSetting`](../../file/task-settings/document-normalizer-task-settings.md), [`OutputTaskSetting`](../../file/task-settings/output-task-setting.md) objects. It is used to define recognition tasks such as reading barcodes, recognizing labels, or detecting document quads.

## Example

```json
{
    "TaskSettingNameArray": ["dbr_task", "dlr_task", "ddn_task"]
}
```

## Parameter Summary

| TaskSettingNameArray Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element represents the name of a `BarcodeReaderTaskSetting` object, `LabelRecognizerTaskSetting` object, `DocumentNormalizerTaskSetting` object, or `OutputTaskSetting` object. |
| **Default Value**<br>	["dbr_task_default", "dlr_task_default", "ddn_task_default"] |
| **Remarks**<br>If `TaskSettingNameArray` is not specified, a default array ["dbr_task_default", "dlr_task_default", "ddn_task_default"] will be created. The TargetROIDef object will have a default configuration of tasks including one barcode reading task, one label recognition task, and one document normalizer task.|
