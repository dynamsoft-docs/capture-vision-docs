---
layout: default-layout
title: BaseImageParameterName - Dynamsoft Capture Vision Parameters
description: The parameter BaseImageParameterName of Dynamsoft Capture Vision is for Inheritancing parameters from a ImageParameter object.
keywords: BaseImageParameterName, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /parameters/reference/image-parameter/base-image-parameter-name.html
---

# BaseImageParameterName

Parameter `BaseImageParameterName` represents the name of another `ImageParameter` object. It is used to inherit the parameters defined in its parent `ImageParameter` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## Example

```json
{
    "BaseImageParameterName": "IP_0"
}
```

## Parameter Summary

| BaseImageParameterName Parameter Summary |
| :---------------------------------- |
| **Description**<br>Name of the ImageParameter object to inherit. |
| **Type**<br>*String* |
| **Value range**<br>One of the ImageParameter name. |
| **Default Value**<br>"" |
