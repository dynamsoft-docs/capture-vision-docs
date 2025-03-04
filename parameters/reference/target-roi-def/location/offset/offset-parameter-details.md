---
layout: default-layout
title:  Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Offset Parameter Details

## ReferenceObjectOriginIndex

Defines which point of the reference object will be set as the origin of the coordinate system.

| ReferenceObjectOriginIndex Parameter Details |
| :------------------- |
| **Type**<br>*int* |
| **Value Range**<br>[0,3] |
| **Default Value**<br>0 |

## ReferenceObjectType

Defines which coordinate system to use when configuring offset parameters basd on the reference objects.

| ReferenceObjectType Parameter Details |
| :------------------- |
| **Type**<br>*String* |
| **Value Range**<br>"ROT_ATOMIC_OBJECT" or "ROT_WHOLE_IMAGE" |
| **Default Value**<br>"ROT_ATOMIC_OBJECT" |

## MeasuredByPercentage

Sets whether or not to use percentage to measure the points' coordinates.

| MeasuredByPercentage Parameter Details |
| :------------------- |
| **Type**<br>*int* |
| **Range**<br>0 or 1 |
| **Default Value**<br>1 |
| **Remarks**<br>0: not by percentage <br>1: by percentage |

## FirstPoint

Specifies the top-left vertex of the ROI with two possible expression forms:

* `[X, Y]`: Represents the coordinates on the x and y axes. The expression in percentage for x and y is determined by parameter `MeasuredByPercentage`.
* `[X, Y, MeasuredXByPercentage, MeasuredYByPercentage]`: Includes independent control over whether the values for x and y are expressed in percentage. `MeasuredXByPercentage` determines if the x-value is in percentage, and `MeasuredYByPercentage` controls the y-value.

| FirstPoint Parameter Details |
| :------------------- |
| **Type**<br>*int[2]* or *int[4]* |
| **Default Value**<br>null |

## SecondPoint

Specifies the top-right vertex of the ROI with two possible expression forms:

* `[X, Y]`: Represents the coordinates on the x and y axes. The expression in percentage for x and y is determined by parameter `MeasuredByPercentage`.
* `[X, Y, MeasuredXByPercentage, MeasuredYByPercentage]`: Includes independent control over whether the values for x and y are expressed in percentage. `MeasuredXByPercentage` determines if the x-value is in percentage, and `MeasuredYByPercentage` controls the y-value.

| FirstPoint Parameter Details |
| :------------------- |
| **Type**<br>*int[2]* or *int[4]* |
| **Default Value**<br>null |

## ThirdPoint

Specifies the bottom-right vertex of the ROI with two possible expression forms:

* `[X, Y]`: Represents the coordinates on the x and y axes. The expression in percentage for x and y is determined by parameter `MeasuredByPercentage`.
* `[X, Y, MeasuredXByPercentage, MeasuredYByPercentage]`: Includes independent control over whether the values for x and y are expressed in percentage. `MeasuredXByPercentage` determines if the x-value is in percentage, and `MeasuredYByPercentage` controls the y-value.

| FirstPoint Parameter Details |
| :------------------- |
| **Type**<br>*int[2]* or *int[4]* |
| **Default Value**<br>null |

## FourthPoint

Specifies the bottom-left vertex of the ROI with two possible expression forms:

* `[X, Y]`: Represents the coordinates on the x and y axes. The expression in percentage for x and y is determined by parameter `MeasuredByPercentage`.
* `[X, Y, MeasuredXByPercentage, MeasuredYByPercentage]`: Includes independent control over whether the values for x and y are expressed in percentage. `MeasuredXByPercentage` determines if the x-value is in percentage, and `MeasuredYByPercentage` controls the y-value.

| FirstPoint Parameter Details |
| :------------------- |
| **Type**<br>*int[2]* or *int[4]* |
| **Default Value**<br>null |
