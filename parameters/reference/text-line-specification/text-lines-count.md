---
layout: default-layout
title: TextLinesCount - Dynamsoft Label Recognizer Parameters
description: The parameter TextLinesCount defines the expected number of text lines for the TextLineSpecification object.
keywords: TextLinesCount
---

# TextLinesCount

Parameter `TextLinesCount` defines the expected number of text lines for the `TextLineSpecification` object.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── TextLinesCount
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "TextLinesCount": 3
}
```

> [!NOTE]
> - This snippet shows only the `TextLinesCount` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br>0. It represents the total number of text lines in the group. |
