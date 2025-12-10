---
layout: default-layout
title: BaseImageParameterName - Dynamsoft Capture Vision Parameters
description: The parameter BaseImageParameterName of Dynamsoft Capture Vision is for inheriting parameters from an ImageParameter object.
keywords: BaseImageParameterName, parameter reference, parameter
---

# BaseImageParameterName

Parameter `BaseImageParameterName` represents the name of another `ImageParameter` object. It is used to inherit the parameters defined in its parent `ImageParameter` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── BaseImageParameterName
```

**Parent object:** [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "BaseImageParameterName": "ip_0"
}
```

> [!NOTE]
> - This snippet shows only the `BaseImageParameterName` parameter.
> - To use it, embed this parameter within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Parameter Details |
| :---------------------------------- |
| **Type**<br>*String* |
| **Value Range**<br>One of the ImageParameter name. |
| **Default Value**<br>`""` |
| **Remarks**<br>The default value "" means this object don't inherit the settings of another object. |
