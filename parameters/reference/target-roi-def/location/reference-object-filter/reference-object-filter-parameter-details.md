---
layout: default-layout
title: ReferenceObjectFilter Parameter Details - Dynamsoft Capture Vision Parameters
description: Details of several ReferenceObjectFilter parameters in Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needGenerateH3Content: true
---
# ReferenceObjectFilter Parameter Details

## ReferenceTargetROIDefNameArray

Filter the reference object by specifying `TargetROI` names.

| ReferenceTargetROIDefNameArray Parameter Details |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be a name of `TargetROI` that defined in `TargetROIDefOptions`. |
| **Default Value**<br>null |

## AtomicResultTypeArray

Filter the reference object by specifying the type of atomic results. In the `TargetROIs` algorithm task can produce atomic results that can support the localization of the other `TargetROIs`.

| AtomicResultTypeArray Parameter Details |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be one of the `AtomicResultType`, which are `ART_TEXT_LINE`, `ART_BARCODE`, `ART_FRAME`, `ART_TABLE_CELL`, `ART_GEOMETRY_LINE`, `ART_CORNER`, `ART_COLOUR_REGION`, and `ART_IMAGE` |
| **Default Value**<br>["ART_TEXT_LINE","ART_BARCODE","ART_FRAME"] |

## ReferenceTaskNameArray

Filter the reference object by specifying the reference task name array.

| AtomicResultTypeArray Parameter Details |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be one of the task in the reference TargetROIDef object array. |
| **Default Value**<br>null |
