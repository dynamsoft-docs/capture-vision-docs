---
layout: default-layout
Title: MaxThreadsInOneTask - Dynamsoft Capture Vision Shared Parameters
Description: The parameter MaxThreadsInOneTask defines the maximum threads that can be consumed in one task.
Keywords: Max threads
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/shared-parameter/max-threads-in-one-task.html
---

# MaxThreadsInOneTask

Parameter `MaxThreadsInOneTask` defines the maximum threads that can be consumed in one task.

```json
{
    "MaxThreadsInOneTask":4
}
```

| MaxThreadsInOneTask Parameter Summary |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 4] |
| **Default Value**<br>4 |

> Note: Parameter `MaxThreadsInOneTask` is available for  `BarcodeReaderTaskSetting`, `LabelRecognizerTaskSetting` and `DocumentNormalizerTaskSetting`. They have the same parameter type, range and default value.
