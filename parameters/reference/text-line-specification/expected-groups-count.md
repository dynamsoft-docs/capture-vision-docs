---
layout: default-layout
title: ExpectedGroupsCount - Dynamsoft Label Recognizer Parameters
description: The parameter ExpectedGroupsCount defines the expected number of TextLineGroups to be found.
keywords: expected groups count
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# ExpectedGroupsCount

The parameter `ExpectGroupsCount` indicates the expected number of `TextLineGroups` to be found. Each `TextLineGroup` is a collection formed by spatially continuous text lines.

## Example

```json
{
    "ExpectedGroupsCount": 1,
}
```

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>int |
| **Default Value**<br>1 |
| **Remarks**<br>1 indicates that only one `TextLineGroup` is expected.<br>0 means no limit is set.|
