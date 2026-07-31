---
layout: default-layout
title: ReferenceObjectFilter Parameter Details - Dynamsoft Capture Vision Parameters
description: Detailed reference for the ReferenceObjectFilter sub-parameters in Dynamsoft Capture Vision, covering ReferenceTargetROIDefNameArray, AtomicResultTypeArray (barcode, text line, frame, etc.), and ReferenceTaskNameArray.
keywords: Location
needGenerateH3Content: true
---
# ReferenceObjectFilter Parameter Details

## ReferenceTargetROIDefNameArray

Filter the reference object by specifying `TargetROI` names.

| ReferenceTargetROIDefNameArray Parameter Details |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be the name of a `TargetROIDef` object that is defined in `TargetROIDefOptions`. |
| **Default Value**<br>null |

## AtomicResultTypeArray

Filter the reference object by specifying the type of atomic results. In the `TargetROIs` algorithm task can produce atomic results that can support the localization of the other `TargetROIs`.

| AtomicResultTypeArray Parameter Details |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be one of the `AtomicResultType`, which are `ART_TEXT_LINE`, `ART_BARCODE`, `ART_FRAME`, `ART_TABLE_CELL`, `ART_GEOMETRY_LINE`, `ART_CORNER`, `ART_COLOUR_REGION`, and `ART_IMAGE` |
| **Default Value**<br>["ART_TEXT_LINE","ART_BARCODE","ART_FRAME"] |

## ReferenceTaskNameArray

Filter the reference object by specifying `TaskSetting` names.

| ReferenceTaskNameArray Parameter Details |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be the name of a `TaskSetting` object. |
| **Default Value**<br>null |
| **Remarks**<br>`ReferenceTargetROIDefNameArray` must be specified and the task must be referenced in these `TargetROIDef` objects.|
