---
layout: default-layout
title: StringLengthRange - Dynamsoft Label Recognizer Parameters
description: The parameter StringLengthRange of text line specification is for specifying the length range of the text line strings.
keywords: string length range, parameter reference, parameter
---

# StringLengthRange

Sets the range of string length for each recognized line.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── StringLengthRange
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "StringLengthRange": [3, 50]
}
```

> [!NOTE]
> - This snippet shows only the `StringLengthRange` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int[]* |
| **Range**<br>The array contains only two elements, corresponding to the lower and upper bounds of the Range, respectively. The value range is [0, 0x7fffffff]. |
| **Default Value**<br>[3,50] |
| **Remarks**<br>An int array defines `MinValue` and `MaxValue` as the range of string length for each recognized line. Default values will be used if there is no manual setting. |
