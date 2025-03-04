---
layout: default-layout
title: TextLineSpecificationNameArray - Dynamsoft Label Recognizer Parameters
description: The parameter TextLineSpecificationNameArray of Dynamsoft Label Recognizer defines the collection of text line specification object names
keywords: text line specification, LabelRecognizerTaskSetting
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextLineSpecificationNameArray

Parameter `TextLineSpecificationNameArray` defines the collection of text line specification object names, used to refer to the `TextLineSpecification` objects

## Example

```json
{
    "TextLineSpecificationNameArray": ["tls_default"]
}
```

## Parameter Summary

| TextLineSpecificationNameArray Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element is the name of a `TextLineSpecification` object. |
| **Default Value**<br>['tls_default'] |
| **Remarks**<br>If `TextLineSpecificationNameArray` is not specified, a default array ["tls_default"] will be created. The TextLineSpecification object with the name "tls_default" will have a default configuration for all text lines.|
