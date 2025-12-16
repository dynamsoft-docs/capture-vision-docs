---
layout: default-layout
title: SemanticProcessingNameArray - Dynamsoft Capture Vision Parameters
description: The parameter SemanticProcessingNameArray of Dynamsoft Capture Vision defines the collection of semantic-processing object names.
keywords: sematic processing, CaptureVisionTemplate
permalink: /parameters/reference/capture-vision-template/semantic-processing-name-array.html
---
# SemanticProcessingNameArray

Parameter `SemanticProcessingNameArray` represents the collection of semantic-processing object names, used to refer to the `SematicProcessing` objects. It is used to define post-processing code parsing tasks performed on input text/bytes.

## JSON Structure

**Location in template:**
```
CaptureVisionTemplates[i]
    └── SemanticProcessingNameArray
```

**Parent object:** [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object

**Example:**

```json
{
    "SemanticProcessingNameArray": ["smp_1"]
}
```

> [!NOTE]
> - This snippet shows only the `SemanticProcessingNameArray` parameter.
> - To use it, embed this parameter within a [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| SemanticProcessingNameArray Parameter Details |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element is the name of a `SematicProcessing` object. |
| **Default Value**<br>null |
