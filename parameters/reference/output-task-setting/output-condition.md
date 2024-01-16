---
layout: default-layout
title: OutputCondition - Dynamsoft Capture Vision OutputSetting Object
description: The parameter OutputCondition of OutputSetting object defines the OutputCondition information of the ROIs.
keywords: OutputCondition
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/output-task-setting/output-condition.html
---

# OutputCondition

The parameter `OutputCondition` defines how the [`OutputTaskSetting`](../../file/task-settings/output-task-setting.md) object outputs results that satisfy multiple filter conditions across products.

## Example

```json
{
    "OutputCondition": {
        "TaskResultArray": [
            {
                "TargetROIDefName": "B", 
                "TaskSettingNameArray": ["B_task"],
                "Operator": "AND",

                "BackwardReferenceOutput": {
                    "ReferenceTaskNameArray": ["A_task"], 
                    "ReferenceResultTypeArray":[ "ART_TEXT_LINE","ART_BARCODE","ART_FRAME", "ART_TABLE_CELL", "ART_COLOUR_REGION" ]
                }
            }
        ],
        "Operator": "AND"
    }
}
```

## Parameter Summary

### TaskResultArray

The parameter `TaskResultArray` configures multiple tasks of descendant `TargetROIDef` objects to filter out the results of the tasks of the reference `TargetROIDef`.

### Operator

The parameter `Operator` defines the type of filtered combination of results from multiple tasks within a `TargetROIDef` object or across multiple `TargetROIDef` objects.

| Operator Parameter Summary |
| :------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the following values: "OR", "AND" |
| **Default Value**<br>"AND"|

#### TargetROIDefName

The parameter `TargetROIDefName` configures the name of descendant `TargetROIDef` object.

| TargetROIDefName Parameter Summary |
| :------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the names of descendant `TargetROIDef` object |
| **Default Value**<br>mandatory|

#### TaskSettingNameArray

The parameter `TaskSettingNameArray` specifies the task name array on the descendant `TargetROIDef` object.

| TaskSettingNameArray Parameter Summary |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member of the array should be one of the task in the descendant `TargetROIDef` object. |
| **Default Value**<br>null|

#### BackwardReferenceOutput

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">ReferenceTaskNameArray</td>
        <td><b>Description</b><br>Specifies the task name array on the TargetROIDef object.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String[]</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>Each member of the array should be one of the task in the reference `TargetROIDef` object.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">ReferenceResultTypeArray</td>
        <td><b>Description</b><br>Specifies the type of atomic results produced by tasks (except OutputTask) on the TargetROIDef object.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String[]</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>Each member should be one of the `AtomicResultType`, which are `ART_TEXT_LINE`, `ART_BARCODE`, `ART_FRAME` and `ART_COLOUR_REGION`
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>["ART_TEXT_LINE","ART_BARCODE","ART_FRAME"]
        </td>
    </tr>
</table>
