---
layout: default-layout
title: ConcatResults - Dynamsoft Label Recognizer Parameters
description: The parameter ConcatResults defines whether to concatenate the output results of the TextLineSpecification object.
keywords: top-level object, ConcatResults
---

# ConcatResults

Parameter `ConcatResults` defines whether to concatenate multiple lines of text. For example, if two lines of text are recognized in a label, the results will be concatenated into one line using `ConcatSeparator` as the separator.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── ConcatResults
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "ConcatResults": 0
}
```

> [!NOTE]
> - This snippet shows only the `ConcatResults` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int* |
| **Range**<br>0,1 |
| **Default Value**<br>0. It does not concat the text line result for the `TextLineSpecification` object. |
