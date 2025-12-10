---
layout: default-layout
title: ConcatSeparator - Dynamsoft Label Recognizer Parameters
description: The parameter ConcatSeparator defines the concat separator of the TextLineSpecification object.
keywords: top-level object, ConcatSeparator
---

# ConcatSeparator

Parameter `ConcatSeparator` defines the concat separator used to join multiple lines of text. For example, if two lines of text are recognized in a label, the results will be concatenated into one line using `ConcatSeparator` as the separator.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── ConcatSeparator
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "ConcatSeparator": "\n"
}
```

> [!NOTE]
> - This snippet shows only the `ConcatSeparator` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>"\n". It represents the connection separator that joins text.|
