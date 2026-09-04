---
layout: default-layout
title: OutputTaskSetting Parameters - Dynamsoft Capture Vision
description: Reference index for OutputTaskSetting object in Dynamsoft Capture Vision parameters, which configure how to output expected results by filtering descendant TargetROIDef results.
keywords: OutputTaskSetting, output, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# OutputTaskSetting Parameters

The `OutputTaskSetting` object configures how to output the expected results of a `TargetROIDef` by filtering the results of descendant `TargetROIDef` objects.

## Example JSON

```json
{
    "OutputTaskSettingOptions": [
        {
            "Name": "output_task",
            "OutputCondition": {
                "TaskResultArray": [
                    {
                        "TargetROIDefName": "B",
                        "TaskSettingNameArray": ["B_task"],
                        "Operator": "AND"
                    }
                ],
                "Operator": "AND"
            }
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `OutputTaskSetting` object inside `OutputTaskSettingOptions`.

```text
OutputTaskSetting
├── Name
└── OutputCondition
```

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the OutputTaskSetting object. |
| [`OutputCondition`](output-condition.md) | The condition for outputting results. |


