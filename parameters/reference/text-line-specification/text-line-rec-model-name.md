---
layout: default-layout
title: TextLineRecModelName - Dynamsoft Label Recognizer Parameters
description: The TextLineRecModelName parameter references the text line recognition model by its name.
keywords: Text line recognition model
---

# TextLineRecModelName

The `TextLineRecModelName` parameter references the text line recognition model by its name.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── TextLineRecModelName
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "TextLineRecModelName": "MRZTextLineRecognition"
}
```

> [!NOTE]
> - This snippet shows only the `TextLineRecModelName` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)



## Parameter Details

| TextLineRecModelName Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The name of a Text Line Recognition Model object that defined in `CaptureVisionModelOptions`. |
| **Default Value**<br>"" |
