---
layout: default-layout
title: Location - Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needGenerateH3Content: true
---
# Location

Parameter `Location` defines the location of the TargetROI with `reference objects` filter conditions and `offset` parameters.

## JSON Structure

**Location in template:**
```
TargetROIDefOptions[i]
    └── Location
```

**Parent object:** [TargetROIDef]({{ site.dcvb_parameters }}file/target-roi-def/index.html) object

**Example:**

```json
{
    "Location": 
    {
        "ReferenceObjectFilter" : {...},
        "Offset": { ... }
    }
}
```

> [!NOTE]
> - This snippet shows only the `Location` parameter.
> - To use it, embed this parameter within a [TargetROIDef]({{ site.dcvb_parameters }}file/target-roi-def/index.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)
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
