---
layout: default-layout
title: OutputTaskSetting - Dynamsoft Capture Vision Parameter File
description: The OutputTaskSetting object in the Dynamsoft Capture Vision Parameter File. 
needAutoGenerateSidebar: false
---

# OutputTaskSetting Object

The `OutputTaskSetting` object is used to configure how to output the expected results of the ancestor `TargetROIDef` by filtering the results of the descendant `TargetROIDef` objects.

## Example

```json
{
    "Name": "output_task",
    "OutputCondition": {
        "TaskResultArray": [
            {
                "TargetROIDefName": "B",
                "TaskSettingNameArray": ["B_task"],
                "Operator": "AND",
                "BackwardReferenceOutput": {
                    "ReferenceTaskNameArray": ["A_task"],
                    "ReferenceResultTypeArray": ["ART_TEXT_LINE", "ART_BARCODE", "ART_FRAME", "ART_TABLE_CELL", "ART_COLOUR_REGION"]
                }
            }
        ],
        "Operator": "AND"
    }
}
```

## Parameters

| Parameter Name | Type | Required/Optional | Description |
|---|---|---|---|
| [`Name`]({{site.dcvb_parameters_reference}}output-task-setting/name.html) | String | Required | The unique identifier for this `OutputTaskSetting` object. |
| [`OutputCondition`]({{site.dcvb_parameters_reference}}output-task-setting/output-condition.html) | Object | Optional | Defines how to filter and output results based on multiple conditions across descendant ROIs. |

## OutputCondition Design

### Key Concepts

| Concept | Description |
|:--------|:------------|
| **Reference TargetROIDef** | The parent `TargetROIDef` object where the output task is located. It serves as the reference point for descendant ROIs. |
| **Descendant TargetROIDef** | Child `TargetROIDef` objects whose task results can be linked back to the reference `TargetROIDef` for filtering. |

### Complete Example

The following example demonstrates a complete `OutputCondition` configuration:

```json
{
    "TargetROIDefOptions": [
        {
            "Name": "A_roi",
            "TaskSettingNameArray": ["ddn_task", "output_task"]
        },
        {
            "Name": "B_roi",
            "TaskSettingNameArray": ["dbr_task"],
            "Location": {
                "ReferenceObjectFilter": {
                    "ReferenceTargetROIDefNameArray": ["A_roi"],
                    "ReferenceTaskNameArray": ["ddn_task"]
                }
            }
        },
        {
            "Name": "C_roi",
            "TaskSettingNameArray": ["dlr_task"],
            "Location": {
                "ReferenceObjectFilter": {
                    "ReferenceTargetROIDefNameArray": ["A_roi"],
                    "ReferenceTaskNameArray": ["ddn_task"]
                }
            }
        }
    ],
    "OutputTaskSettingOptions": [
        {
            "Name": "output_task",
            "OutputCondition": {
                "TaskResultArray": [
                    {
                        "TargetROIDefName": "B_roi",
                        "BackwardReferenceOutput": {
                            "ReferenceTaskNameArray": ["ddn_task"]
                        }
                    },
                    {
                        "TargetROIDefName": "C_roi",
                        "BackwardReferenceOutput": {
                            "ReferenceTaskNameArray": ["ddn_task"]
                        }
                    }
                ],
                "Operator": "AND"
            }
        }
    ]
}
```

<div align="center">
   <p><img src="../assets/output-task-setting.png" alt="OutputTaskSetting example" width="80%" /></p>
</div>

**In this example:**
- **Parent ROI:** `A_roi` contains tasks `ddn_task` and `output_task`
- **Descendant ROIs:** `B_roi` (with `dbr_task`) and `C_roi` (with `dlr_task`)
- **Workflow:** `output_task` retrieves results from `B_roi` and `C_roi`, references `ddn_task` results, and applies AND logic for filtering
