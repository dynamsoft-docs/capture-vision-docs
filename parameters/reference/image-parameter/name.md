---
layout: default-layout
title: Name - Dynamsoft Capture Vision Parameter Reference ImageParameter Object.
description: The parameter Name defines the unique identifier of ImageParameter object.
keywords: top-level object, name, unique identifier
---

# Name

Parameter `Name` represents the name of a `ImageParameter` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── Name
```

**Parent object:** [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Name": "ip_0"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Required**<br>Yes |
| **Default Value**<br>N/A |
| **Remarks**<br>It must be a unique name. |
