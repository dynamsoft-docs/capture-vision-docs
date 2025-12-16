---
layout: default-layout
title: BaseTextLineSpecificationName - Dynamsoft Label Recognizer Parameters
description: The parameter BaseTextLineSpecificationName of Dynamsoft Label Recognizer defines the name of base TextLineSpecification object.
keywords: Applicable text line numbers
---

# BaseTextLineSpecificationName

Parameter `BaseTextLineSpecificationName` represents the name of another `BaseTextLineSpecificationName` object. It is used to inherit the parameters defined in its parent `BaseTextLineSpecificationName` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── BaseTextLineSpecificationName
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "BaseTextLineSpecificationName": "LS_0"
}
```

> [!NOTE]
> - This snippet shows only the `BaseTextLineSpecificationName` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| BaseTextLineSpecificationName Parameter Details |
| :----------------------------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the existing `TextLineSpecification` object name. |
| **Default Value**<br>"" |
| **Remarks**<br>The default value "" means this object don't inherit the settings of another object. |
