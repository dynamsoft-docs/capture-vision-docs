---
layout: default-layout
title: Name - Dynamsoft Capture Vision Parameter Reference CaptureVisionTemplate Object.
description: The parameter Name defines the unique identifier of CaptureVisionTemplate object.
keywords: top-level object, name, unique identifier
permalink: /parameters/reference/capture-vision-template/name.html
---
# Name

Parameter `Name` represents the name of a `CaptureVisionTemplate` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
CaptureVisionTemplates[i]
    └── Name
```

**Parent object:** [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object

**Example:**

```json
{
    "Name" : "cv_0"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within a [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |
