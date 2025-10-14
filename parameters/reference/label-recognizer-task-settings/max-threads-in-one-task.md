---
layout: default-layout
title: MaxThreadsInOneTask - Dynamsoft Label Recognizer Parameters
description: The parameter MaxThreadsInOneTask defines the maximum threads that can be consumed in one label recognition task.
keywords: Max threads
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# MaxThreadsInOneTask

Parameter `MaxThreadsInOneTask` defines the maximum threads that can be consumed in one task.

## Example

```json
{
    "MaxThreadsInOneTask":4
}
```

## Parameter Summary

| MaxThreadsInOneTask Parameter Summary |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 256] |
| **Default Value**<br>0 |

**Remarks**

- Changed the default value to 0 from 4 in version 3.2.1000
- Updated the value range to [0, 256] in version 3.2.1000