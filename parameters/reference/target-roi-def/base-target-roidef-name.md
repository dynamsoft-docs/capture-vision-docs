---
layout: default-layout
title: BaseTargetROIDefName - Dynamsoft Capture Vision Parameters
description: The parameter BaseTargetROIDefName of Dynamsoft Capture Vision defines the name of the inherited TargetROIDef object.
keywords: inheritance, TargetROIDef
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/target-roi-def/base-target-roidef-name.html
---

# BaseTargetROIDefName

Parameter `BaseTargetROIDefName` represents the name of another `TargetROIDef` object. It is used to inherit the parameters defined in its parent `TargetROIDef` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## Example

```json
{
    "BaseTargetROIDefName": "roi_1"
}
```

## Parameter Summary

| BaseTargetROIDefName Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of the inherited `TargetROIDef` object. |
| **Default Value**<br>"" |
| **Remarks**<br>(1) "" stands for no inheritance.<br>(2) If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.|
