---
layout: default-layout
Title: BaseTargetROIDefName - Dynamsoft Capture Vision Parameters
Description: The parameter BaseTargetROIDefName of Dynamsoft Capture Vision defines the name of the inherited TargetROIDef object.
Keywords: inheritance, TargetROIDef
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BaseTargetROIDefName

Represents the name of another `TargetROIDef` object. It is used to inherit the parameters defined in its parent `TargetROIDef` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

```json
{
    "BaseTargetROIDefName": "roi_1"
}
```

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of the inherited `TargetROIDef` object. |
| **Default Value**<br>"" |
| **Remarks**<br>(1) "" stands for no inheritance.<br>(2) If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.|
