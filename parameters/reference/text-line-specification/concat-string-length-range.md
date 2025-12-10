---
layout: default-layout
title: ConcatStringLengthRange - Dynamsoft Label Recognizer Parameters
description: The parameter ConcatStringLengthRange of text line specification is for specifying the length range of the text line strings.
keywords: concat string length range, parameter reference, parameter
---

# ConcatStringLengthRange

Sets the range of string length for the concated recognized text lines.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── ConcatStringLengthRange
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "ConcatStringLengthRange": [3, 200]
}
```

> [!NOTE]
> - This snippet shows only the `ConcatStringLengthRange` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int[]* |
| **Range**<br>The array contains only two elements, corresponding to the lower and upper bounds of the Range, respectively. The value range is [3, 0x7fffffff]. |
| **Default Value**<br>[3,200] |
| **Remarks**<br>An int array defines `MinValue` and `MaxValue` as the range of string length for the concated recognized text lines. |
