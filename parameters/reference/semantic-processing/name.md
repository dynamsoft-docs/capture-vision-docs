---
layout: default-layout
title: Name - Dynamsoft Capture Vision semantic processing object
description: The parameter Name defines the unique identifier of SemanticProcessing object.
keywords: top-level object, name, unique identifier, semantic processing
needGenerateH3Content: true
---
# Name

Parameter `Name` represents the name of a `SemanticProcessing` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
SemanticProcessingOptions[i]
    └── Name
```

**Parent object:** [SemanticProcessing]({{ site.dcvb_parameters }}file/semantic-processing/index.html) object

**Example:**

```json
{
    "Name" : "sp_0"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within a [SemanticProcessing]({{ site.dcvb_parameters }}file/semantic-processing/index.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |
