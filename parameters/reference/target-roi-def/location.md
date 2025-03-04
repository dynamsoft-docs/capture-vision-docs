---
layout: default-layout
title: Location - Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/target-roi-def/location.html
---

# Location

Parameter `Location` defines the location of the TargetROI with `reference objects` filter conditions and `offset` parameters.

## Example

```json
{
    "Location": 
    {
        "ReferenceObjectFilter" : {...},
        "Offset": { ... }
    }
}
```

|  Name | Description |
| ---- | ----------- |
| [`ReferenceObjectFilter`](#referenceobjectfilter) | Filter the reference object by specifying `TargetROI` names. |
| [`Offset`](#offset) | Defines how the location is offset from the `reference object` or the original image. |

## ReferenceObjectFilter

Parameter `ReferenceObjectFilter` is a group of filter conditions for figuring out the `reference objects`.

| ReferenceObjectFilter Parameter Details |
| :------------------- |
| **Type**<br>*[ReferenceObjectFilter](location/reference-object-filter/index.md)* Object |

## Offset

Parameter `Offset` is an object that defines how the location is offset from the `reference object` or the original image.

| Offset Parameter Details |
| :------------------- |
| **Type**<br>*[Offset](location/offset/index.md)* Object |
