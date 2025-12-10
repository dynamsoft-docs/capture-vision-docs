---
layout: default-layout
title: ExpectedGroupsCount - Dynamsoft Label Recognizer Parameters
description: The parameter ExpectedGroupsCount defines the expected number of TextLineGroups to be found.
keywords: expected groups count
---

# ExpectedGroupsCount

The parameter `ExpectGroupsCount` indicates the expected number of `TextLineGroups` to be found. Each `TextLineGroup` is a collection formed by spatially continuous text lines.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── ExpectedGroupsCount
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "ExpectedGroupsCount": 1,
}
```

> [!NOTE]
> - This snippet shows only the `ExpectedGroupsCount` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>int |
| **Default Value**<br>1 |
| **Remarks**<br>1 indicates that only one `TextLineGroup` is expected.<br>0 means no limit is set.|
