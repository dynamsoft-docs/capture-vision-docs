---
layout: default-layout
title: Name - Dynamsoft Label Recognizer Parameters TextLineSpecification object
description: The parameter Name defines the unique identifier of TextLineSpecification object.
keywords: top-level object, name, unique identifier
---

# Name

Parameter `Name` represents a `TextLineSpecification` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── Name
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters_reference }}text-line-specification/index.html) object

**Example:**

```json
{
    "Name": "cv_0"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters_reference }}text-line-specification/index.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters_reference }}index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters_reference }}index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |
