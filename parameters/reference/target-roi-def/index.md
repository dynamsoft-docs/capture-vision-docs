---
layout: default-layout
title: TargetROIDef Parameters - Dynamsoft Capture Vision
description: Reference index for TargetROIDef object in Dynamsoft Capture Vision parameters, which specify regions of interest (ROIs) within an image and the recognition tasks to perform on them.
keywords: TargetROIDef, ROI, region of interest, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# TargetROIDef Parameters

The `TargetROIDef` object specifies one or more recognition tasks to be performed on regions of interest (ROIs) within an image.

## Example JSON

```json
{
    "TargetROIDefOptions": [
        {
            "Name": "roi_a",
            "BaseTargetROIDefName": "",
            "TaskSettingNameArray": ["dbr_task"],
            "PauseFlag": 0,
            "EnableResultsDeduplication": 1,
            "Location": {
                "ReferenceObjectFilter": {
                    "ReferenceTargetROIDefNameArray": ["roi_root"],
                    "ReferenceTaskSettingNameArray": ["dbr_root"],
                    "ReferenceResultType": "RRT_ORIGINAL_IMAGE"
                },
                "Offset": {
                    "MeasuredByPercentage": 1,
                    "FirstPoint": [0, 0],
                    "SecondPoint": [100, 100]
                }
            }
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `TargetROIDef` object inside `TargetROIDefOptions`.

```text
TargetROIDef
├── Name
├── BaseTargetROIDefName
├── TaskSettingNameArray
├── PauseFlag
├── EnableResultsDeduplication
└── Location
  ├── ReferenceObjectFilter
  └── Offset
```

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the TargetROIDef object. |
| [`BaseTargetROIDefName`](base-target-roidef-name.md) | The name of another TargetROIDef to inherit from. |
| [`TaskSettingNameArray`](task-setting-name-array.md) | The names of task setting objects to apply. |
| [`PauseFlag`](pause-flag.md) | Whether to pause processing at this ROI. |
| [`EnableResultsDeduplication`](enable-results-deduplication.md) | Whether to enable deduplication of results. |
| [`Location`](location.md) | The location definition of the target ROI. |

## Nested Parameter Quick Links

### Actual Nested Parameters in the Tree

| Parameter Name | Description |
|:---------------|:------------|
| [`ReferenceObjectFilter`](location/reference-object-filter/index.md) | Filters which reference objects are used when computing the ROI location. |
| [`Offset`](location/offset/index.md) | Defines the offset from the reference object to the target ROI. |

### Conceptual Location Objects

| Object | Description |
|:-------|:------------|
| [`Location`](location.md) | Container object that combines reference filtering and offset definition. |


