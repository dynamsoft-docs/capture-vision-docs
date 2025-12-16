---
layout: default-layout
title: BaseDocumentNormalizerTaskSettingName - Dynamsoft Document Normalizer Parameters
description: The parameter BaseDocumentNormalizerTaskSettingName defines the base object of the current DocumentNormalizerTaskSetting.
keywords: Base document normalizer task setting name
---

# BaseDocumentNormalizerTaskSettingName

`BaseDocumentNormalizerTaskSettingName` represents the name of another `DocumentNormalizerTaskSetting` object. It is used to inherit the parameters defined in its parent `DocumentNormalizerTaskSetting` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── BaseDocumentNormalizerTaskSettingName
```

**Parent object:** [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html)

**Example:**

```json
{
    "BaseDocumentNormalizerTaskSettingName": "DD_0"
}
```

> [!NOTE]
> - This snippet shows only the `BaseDocumentNormalizerTaskSettingName` parameter.
> - To use it, embed this parameter within a [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| BaseDocumentNormalizerTaskSettingName Parameter Details |
| :------------------------------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the existing `DocumentNormalizerTaskSetting` object name. |
| **Default Value**<br>"" |
| **Remarks**<br>The default value "" means this object don't inherit the settings of another object. |
