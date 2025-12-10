---
layout: default-layout
title: Name - Dynamsoft Capture Vision TargetROIDef object
description: The parameter Name defines the unique identifier of TargetROIDef object.
keywords: top-level object, name, unique identifier
permalink: /parameters/reference/target-roi-def/name.html
---
# Name

Parameter `Name` represents a `TargetROIDef` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
TargetROIDefOptions[i]
    └── Name
```

**Parent object:** [TargetROIDef]({{ site.dcvb_parameters }}file/target-roi-def/index.html) object

**Example:**

```json
{
    "Name" : "roi_0"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within a [TargetROIDef]({{ site.dcvb_parameters }}file/target-roi-def/index.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |
