---
layout: default-layout
title: OutputCondition - Dynamsoft Capture Vision OutputSetting Object
description: The parameter OutputCondition of OutputSetting object defines the OutputCondition information of the ROIs.
keywords: OutputCondition
---

# OutputCondition

## Overview

The parameter `OutputCondition` defines how the [`OutputTaskSetting`](../../file/task-settings/output-task-setting.md) object outputs results that satisfy multiple filter conditions across products. It allows you to configure complex filtering logic by combining results from multiple tasks and TargetROIDef objects using logical operators (AND/OR).

**Use Cases:**
- Filter outputs based on conditions from descendant TargetROIDef tasks
- Combine results from multiple processing tasks with logical operators
- Reference specific atomic result types from previous tasks

## JSON Structure

**Location in template:**
```
OutputTaskSettingOptions[i]
    └── OutputCondition
```

**Parent object:** [OutputTaskSetting]({{ site.dcvb_parameters }}file/task-settings/output-task-setting.html) object

**Example:**

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

**Example Explanation:**

This configuration filters output results where:
- The top-level `Operator` is "AND", requiring all conditions in `TaskResultArray` to be met
- Results from task "B_task" on TargetROIDef "B" must exist
- These results must have backward references to task "A_task" 
- The referenced results must be one of the specified atomic result types (text lines, barcodes, frames, table cells, or color regions)

> [!NOTE]
> - This snippet shows only the `OutputCondition` parameter.
> - To use it, embed this parameter within a [OutputTaskSetting]({{ site.dcvb_parameters }}file/task-settings/output-task-setting.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

### Operator (Top-Level)

The top-level `Operator` parameter defines how to combine the conditions from multiple items in the `TaskResultArray`. 

| Operator Parameter Details |
| :------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the following values: "OR", "AND" |
| **Default Value**<br>"AND"|

**Explanation:**
- **"AND"**: All conditions in `TaskResultArray` must be satisfied
- **"OR"**: At least one condition in `TaskResultArray` must be satisfied

### TaskResultArray

The parameter `TaskResultArray` is an array that configures multiple filtering conditions based on tasks from descendant `TargetROIDef` objects. Each array element represents one filtering condition.

**Type:** Array of objects

Each object in the array contains the following parameters:

#### TargetROIDefName

Specifies the name of the descendant `TargetROIDef` object to reference.

| TargetROIDefName Parameter Details |
| :------------------- |
| **Type**<br>*String* |
| **Range**<br>Must be one of the descendant `TargetROIDef` object names defined in your template |
| **Default Value**<br>Mandatory (no default)|

#### TaskSettingNameArray

Specifies which tasks on the descendant `TargetROIDef` object to check for results.

| TaskSettingNameArray Parameter Details |
| :------------------- |
| **Type**<br>*String[]* (Array of strings) |
| **Range**<br>Each member must be a valid task name in the specified descendant `TargetROIDef` object |
| **Default Value**<br>null|

#### Operator (Task-Level)

Defines how to combine multiple task results within this specific condition.

| Operator Parameter Details |
| :------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the following values: "OR", "AND" |
| **Default Value**<br>"AND"|

**Note:** This is different from the top-level `Operator`. The task-level operator combines results within a single `TaskResultArray` item, while the top-level operator combines across multiple array items.

#### BackwardReferenceOutput

Configures backward reference filtering based on results from the reference (parent) `TargetROIDef` object.

##### ReferenceTaskNameArray

Specifies which tasks on the reference `TargetROIDef` object to check for backward references.

| ReferenceTaskNameArray Parameter Details |
| :------------------- |
| **Type**<br>*String[]* (Array of strings) |
| **Range**<br>Each member must be a valid task name in the reference `TargetROIDef` object |
| **Default Value**<br>null|

##### ReferenceResultTypeArray

Specifies which types of atomic results to accept from the referenced tasks.

| ReferenceResultTypeArray Parameter Details |
| :------------------- |
| **Type**<br>*String[]* (Array of strings) |
| **Range**<br>Each member must be one of the following `AtomicResultType` values:<br>- `"ART_TEXT_LINE"`: Text line results<br>- `"ART_BARCODE"`: Barcode results<br>- `"ART_FRAME"`: Frame results<br>- `"ART_TABLE_CELL"`: Table cell results<br>- `"ART_COLOUR_REGION"`: Color region results |
| **Default Value**<br>["ART_TEXT_LINE","ART_BARCODE","ART_FRAME"]|

## Terminology

- **Reference TargetROIDef**: The parent or current `TargetROIDef` object that contains the `OutputTaskSetting` with this `OutputCondition`
- **Descendant TargetROIDef**: Child `TargetROIDef` objects that are referenced in the `TaskResultArray`
- **Backward Reference**: A link from a descendant task result back to a parent task result

## Best Practices

1. **Use meaningful names**: Choose descriptive names for TargetROIDef and task settings to make your configuration easier to understand
2. **Start simple**: Begin with a single condition and "AND" operator, then add complexity as needed
3. **Specify result types**: Explicitly set `ReferenceResultTypeArray` to only include the atomic result types you actually need
4. **Test conditions**: Verify that your filter conditions work as expected with sample data before deploying

## See Also

- [OutputTaskSetting]({{ site.dcvb_parameters }}file/task-settings/output-task-setting.html)
- [TargetROIDef]({{ site.dcvb_parameters }}file/target-roi-definition/index.html)
- [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
