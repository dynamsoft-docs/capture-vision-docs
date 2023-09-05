---
layout: default-layout
title: BaseDocumentNormalizerTaskSettingName - Dynamsoft Document Normalizer Parameters
description: The parameter BaseDocumentNormalizerTaskSettingName of Dynamsoft Document Normalizer defines the base object of the current DocumentNormalizerTaskSetting.
keywords: Base document normalizer task setting name
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/document-normalizer-task-settings/base-document-normalizer-task-setting-name.html
---

# BaseDocumentNormalizerTaskSettingName

Parameter `BaseDocumentNormalizerTaskSettingName` represents the name of another `DocumentNormalizerTaskSetting` object. It is used to inherit the parameters defined in its parent `DocumentNormalizerTaskSetting` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## Example

```json
{
    "BaseDocumentNormalizerTaskSettingName": "DD_0"
}
```

## Parameter Summary

| BaseDocumentNormalizerTaskSettingName Parameter Summary |
| :------------------------------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the existing `DocumentNormalizerTaskSetting` object name. |
| **Default Value**<br>"" |
