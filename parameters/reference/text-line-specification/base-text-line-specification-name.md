---
layout: default-layout
Title: BaseTextLineSpecificationName - Dynamsoft Label Recognizer Parameters
Description: The parameter BaseTextLineSpecificationName of Dynamsoft Label Recognizer defines the name of base TextLineSpecification object.
Keywords: Applicable text line numbers
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/text-line-specification/base-text-line-specification-name.html
---

# BaseTextLineSpecificationName

Parameter `BaseTextLineSpecificationName` represents the name of another `BaseTextLineSpecificationName` object. It is used to inherit the parameters defined in its parent `BaseTextLineSpecificationName` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## Example

```json
{
    "BaseTextLineSpecificationName": "LS_0"
}
```

## Parameter Summary

| BaseTextLineSpecificationName Parameter Summary |
| :----------------------------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the existing `TextLineSpecification` object name. |
| **Default Value**<br>"" |
| **Remarks**<br>The default value "" means this object don't inherit the settings of another object. |
