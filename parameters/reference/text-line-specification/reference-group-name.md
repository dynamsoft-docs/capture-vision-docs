---
layout: default-layout
title: ReferenceGroupName - Dynamsoft Label Recognizer Parameters
description: The parameter ReferenceGroupName defines the reference group name of TextLineSpecification object.
keywords: top-level object, reference group name
---

# ReferenceGroupName

Parameter `ReferenceGroupName` can be configured to reference a father, grandfather, uncle, sibling `TextLineSpecification` object, etc., but not descendants. It is used to define the reference group for space layout configuration and affects the following parameters:

- ApplicableTextLineNumbers (Only if the reference group is the parent group)
- FirstPoint
- SecondPoint
- ThirdPoint
- FourthPoint

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── ReferenceGroupName
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "Name" : "tls_0",
    "ApplicableTextLineNumbers": "5-8",
    "SubGroups" : [
        {
            "Name" : "tls_0_0",
            // "1-2" is equivalent to "5-6" for ApplicableTextLineNumbers in the tls_0 group.
            "ApplicableTextLineNumbers": "1-2",
            "ReferenceGroupName" : "tls_0"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `ReferenceGroupName` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>"" |
| **Remarks**<br>It must be the name of the `TextLineSpecification` object. It is configured to reference a father, grandfather, uncle, sibling `TextLineSpecification` object, etc., but not descendants. |
