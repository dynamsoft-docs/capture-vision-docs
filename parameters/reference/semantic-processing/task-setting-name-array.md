---
layout: default-layout
title: TaskSettingNameArray - Dynamsoft Capture Vision Semantic Processing Parameters
description: The parameter TaskSettingNameArray defines the collection of CodeParserTaskSetting object names.
keywords: task settings, semantic processing
needGenerateH3Content: true
---
# TaskSettingNameArray

Parameter `TaskSettingNameArray` represents the collection of task setting object names, used to refer to the [`CodeParserTaskSetting`](../../file/task-settings/code-parser-task-settings.md) objects.

## JSON Structure

**Location in template:**
```
SemanticProcessingOptions[i]
    └── TaskSettingNameArray
```

**Parent object:** [SemanticProcessing]({{ site.dcvb_parameters }}file/semantic-processing.html) object

**Example:**

```json
{
    "TaskSettingNameArray": ["CPT1_PARSE_VIN"]
}
```

> [!NOTE]
> - This snippet shows only the `TaskSettingNameArray` parameter.
> - To use it, embed this parameter within a [SemanticProcessing]({{ site.dcvb_parameters }}file/semantic-processing.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| TaskSettingNameArray Parameter Details |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element represents the name of a `CodeParserTaskSetting` object. |
