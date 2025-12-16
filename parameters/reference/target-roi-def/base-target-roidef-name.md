---
layout: default-layout
title: BaseTargetROIDefName - Dynamsoft Capture Vision Parameters
description: The parameter BaseTargetROIDefName of Dynamsoft Capture Vision defines the name of the inherited TargetROIDef object.
keywords: inheritance, TargetROIDef
permalink: /parameters/reference/target-roi-def/base-target-roidef-name.html
---
# BaseTargetROIDefName

Parameter `BaseTargetROIDefName` represents the name of another `TargetROIDef` object. It is used to inherit the parameters defined in its parent `TargetROIDef` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## JSON Structure

**Location in template:**
```
TargetROIDefOptions[i]
    └── BaseTargetRoidefName
```

**Parent object:** [TargetROIDef]({{ site.dcvb_parameters }}file/target-roi-definition/index.html) object

**Example:**

```json
{
    "BaseTargetROIDefName": "roi_1"
}
```

> [!NOTE]
> - This snippet shows only the `BaseTargetRoidefName` parameter.
> - To use it, embed this parameter within a [TargetROIDef]({{ site.dcvb_parameters }}file/target-roi-definition/index.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| BaseTargetROIDefName Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of the inherited `TargetROIDef` object. |
| **Default Value**<br>"" |
| **Remarks**<br>(1) "" stands for no inheritance.<br>(2) If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.|
