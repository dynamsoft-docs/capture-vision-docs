---
layout: default-layout
title: SubGroups - Dynamsoft Label Recognizer Parameters
description: The parameters SubGroups defines the layout of subgroups of the TextLineSpecification object.
keywords: SubGroups
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/text-line-specification/sub-groups.html
---

# SubGroups

Parameter `SubGroups` defines the layout of subgroups of the `TextLineSpecification` object. It can be nested recursively defined.

## Example

```json
{
    "Name": "tls_0",
    "ApplicableTextLineNumbers": "3-7",
    "SubGroups" : [
        {
            "Name": "tls_0_0",
            "ApplicableTextLineNumbers": "3-5",
            "SubGroups" : [
                {
                    "Name": "tls_0_0_0",
                    "ApplicableTextLineNumbers": "4"
                }
            ]
        },
        {
        }
    ]
}
```

<div align="center">
   <p><img src="../assets/text-line-group-example.png" alt="SubGroups example" width="80%" /></p>
</div>

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*Array* |
| **Range**<br>Array of `TextLineSpecification` Object |
| **Default Value**<br>null. It means that there are no definitions in the subgroups of this `TextLineSpecification` object. |
