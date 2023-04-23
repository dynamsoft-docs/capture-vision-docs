---
layout: default-layout
Title: BaseTargetROIDefName - Dynamsoft Capture Vision Parameters
Description: The parameter BaseTargetROIDefName of Dynamsoft Capture Vision defines the name of the inherited TargetROIDef object.
Keywords: inheritance, TargetROIDef
needAutoGenerateSidebar: true
noTitleIndex: true
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
