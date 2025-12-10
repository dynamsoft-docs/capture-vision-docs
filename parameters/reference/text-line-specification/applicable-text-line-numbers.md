---
layout: default-layout
title: ApplicableTextLineNumbers - Dynamsoft Label Recognizer Parameters
description: The parameter ApplicableTextLineNumbers of Dynamsoft Label Recognizer defines the line numers of the targeting text lines.
keywords: Applicable text line numbers
---

# ApplicableTextLineNumbers

Parameter `ApplicableTextLineNumbers` specifies the line numbers of the targeting lines which are specified by the `TextLineSpecification` object.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── ApplicableTextLineNumbers
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "ApplicableTextLineNumbers": "1-10"
}
```

> [!NOTE]
> - This snippet shows only the `ApplicableTextLineNumbers` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| ApplicableTextLineNumbers Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>A string of one or more of the following data:<br>1. One int value which represents a specified line index;<br>2. One Expression, start index and stop index connected with ""-"", which represents a specified line index range. |
| **Default Value**<br>"" |
| **Remarks**<br>(1) The value is 1-based.<br>(2) "" represents all lines.<br>(3) The processed of the not specified text lines will implement the default settings.<br>(4) If the line number you specified doesn't exist, the library will ignore it. |
