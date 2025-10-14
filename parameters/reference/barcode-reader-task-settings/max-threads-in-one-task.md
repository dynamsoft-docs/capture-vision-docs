---
layout: default-layout
title: MaxThreadsInOneTask - Dynamsoft Barcode Reader Parameters
description: The parameter MaxThreadsInOneTask defines the maximum threads that can be consumed in one barcode reader task.
keywords: Max threads
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

- Changed the default value to 0 from 4 in version 11.2.1000
- Updated the value range to [0, 256] in version 11.2.1000