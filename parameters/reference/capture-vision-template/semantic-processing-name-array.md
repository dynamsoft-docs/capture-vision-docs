---
layout: default-layout
title: SemanticProcessingNameArray - Dynamsoft Capture Vision Parameters
description: The parameter SemanticProcessingNameArray of Dynamsoft Capture Vision defines the collection of semantic-processing object names.
keywords: sematic processing, CaptureVisionTemplate
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /parameters/reference/capture-vision-template/semantic-processing-name-array.html
---

# SemanticProcessingNameArray

Parameter `SemanticProcessingNameArray` represents the collection of semantic-processing object names, used to refer to the `SematicProcessing` objects. It is used to define post-processing code parsing tasks performed on input text/bytes.

## Example

```json
{
    "SemanticProcessingNameArray": ["smp_1"]
}
```

## Parameter Summary

| SemanticProcessingNameArray Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element is the name of a `SematicProcessing` object. |
| **Default Value**<br>null |
