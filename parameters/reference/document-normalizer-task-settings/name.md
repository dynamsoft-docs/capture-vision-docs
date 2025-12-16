---
layout: default-layout
title: Name - Dynamsoft Document Normalizer DocumentNormalizerTaskSetting Parameters
description: The parameter Name defines the unique identifier of a DocumentNormalizerTaskSetting object.
keywords: top-level object, name, unique identifier
---

# Name

`Name` represents the name of a `DocumentNormalizerTaskSetting` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── Name
```

**Parent object:** [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html)

**Example:**

```json
{
    "Name": "dn_0"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within a [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |
