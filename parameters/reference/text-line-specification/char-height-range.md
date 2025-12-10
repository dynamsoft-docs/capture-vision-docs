---
layout: default-layout
title: CharHeightRange - Dynamsoft Label Recognizer Parameters
description: The parameter CharHeightRange of Dynamsoft Label Recognizer defines the range of the character height.
keywords: Applicable text line numbers
---

# CharHeightRange

Parameter `CharHeightRange` defines the range of the character height (in pixel or a percentage value relative to the height of the `targetROI`).

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── CharHeightRange
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "CharHeightRange": [ 800, 1000, 1 ]
}
```

> [!NOTE]
> - This snippet shows only the `CharHeightRange` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| CharHeightRange Parameter Details |
| :-------------------------------- |
| **Type**<br>*int Array* |
| **Range**<br>The third member should be 0 or 1, which determines whether the range is measured by thousandth. If measured by thousandth, the first 2 members should be int values between 1 to 1000. Otherwise, they should between 1 to 0x7fffffff. |
| **Default Value**<br>"" |
| **Remarks**<br>Format: [MinHeight, MaxHeight, ByThousandth]. |
