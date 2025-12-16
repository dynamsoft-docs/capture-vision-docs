---
layout: default-layout
title: TextLineSpecificationNameArray - Dynamsoft Label Recognizer Parameters
description: The parameter TextLineSpecificationNameArray defines the collection of text line specification object names.
keywords: text line specification, LabelRecognizerTaskSetting
---

# TextLineSpecificationNameArray

`TextLineSpecificationNameArray` defines the collection of text line specification object names, used to refer to the `TextLineSpecification` objects.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── TextLineSpecificationNameArray
```

**Parent object:** [LabelRecognizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/label-recognizer-task-settings.html)

**Example:**

```json
{
    "TextLineSpecificationNameArray": ["tls_default"]
}
```

> [!NOTE]
> - This snippet shows only the `TextLineSpecificationNameArray` parameter.
> - To use it, embed this parameter within a [LabelRecognizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/label-recognizer-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| TextLineSpecificationNameArray Parameter Details |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element is the name of a `TextLineSpecification` object. |
| **Default Value**<br>['tls_default'] |
| **Remarks**<br>If `TextLineSpecificationNameArray` is not specified, a default array ["tls_default"] will be created. The `TextLineSpecification` object with the name "tls_default" will have a default configuration for all text lines.|
