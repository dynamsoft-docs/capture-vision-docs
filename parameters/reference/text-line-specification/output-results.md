---
layout: default-layout
title: OutputResults - Dynamsoft Label Recognizer Parameters
description: The parameter OutputResults defines whether to enable the output of the TextLineSpecification object.
keywords: top-level object, OutputResults
---

# OutputResults

Parameter `OutputResults` defines whether to enable the output of the `TextLineSpecification` object.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── OutputResults
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "OutputResults": 0
}
```

> [!NOTE]
> - This snippet shows only the `OutputResults` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int* |
| **Range**<br>0,1 |
| **Default Value**<br>1. It outputs the text line result for the `TextLineSpecification` object. |
