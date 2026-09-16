---
layout: default-layout
title: TaskSettingNameArray - Dynamsoft Capture Vision Parameters
description: Reference for the TaskSettingNameArray parameter in the Dynamsoft Capture Vision TargetROIDef object, which lists the names of task setting objects (BarcodeReaderTaskSetting, LabelRecognizerTaskSetting, DocumentNormalizerTaskSetting, or OutputTaskSetting) to execute on the target ROI.
keywords: task settings, TargetROIDef
---
# TaskSettingNameArray

Parameter `TaskSettingNameArray` represents the collection of task setting object names, used to refer to the [`BarcodeReaderTaskSetting`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/index.html),[`LabelRecognizerTaskSetting`]({{ site.dcvb_parameters_reference }}label-recognizer-task-settings/index.html),[`DocumentNormalizerTaskSetting`]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/index.html), [`OutputTaskSetting`]({{ site.dcvb_parameters_reference }}output-task-setting/index.html) objects. It is used to define recognition tasks such as reading barcodes, recognizing labels, or detecting document quads.

## JSON Structure

**Location in template:**
```
TargetROIDefOptions[i]
    └── TaskSettingNameArray
```

**Parent object:** [TargetROIDef]({{ site.dcvb_parameters_reference }}target-roi-def/index.html) object

**Example:**

```json
{
    "TaskSettingNameArray": ["dbr_task", "dlr_task", "ddn_task"]
}
```

> [!NOTE]
> - This snippet shows only the `TaskSettingNameArray` parameter.
> - To use it, embed this parameter within a [TargetROIDef]({{ site.dcvb_parameters_reference }}target-roi-def/index.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters_reference }}index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters_reference }}index.html#minimal-valid-json-example)

## Parameter Details

| TaskSettingNameArray Parameter Details |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element represents the name of a `BarcodeReaderTaskSetting` object, `LabelRecognizerTaskSetting` object, `DocumentNormalizerTaskSetting` object, or `OutputTaskSetting` object. |
| **Default Value**<br>	["dbr_task_default", "dlr_task_default", "ddn_task_default"] |
| **Remarks**<br>If `TaskSettingNameArray` is not specified, a default array ["dbr_task_default", "dlr_task_default", "ddn_task_default"] will be created. The `TargetROIDef` object will have a default configuration of tasks including one barcode reading task, one label recognition task, and one document normalizer task.|
