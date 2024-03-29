---
layout: default-layout
title: MaxThreadsInOneTask - Dynamsoft Capture Vision Shared Parameters
description: The parameter MaxThreadsInOneTask defines the maximum threads that can be consumed in one task.
keywords: Max threads
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/shared-parameter/max-threads-in-one-task.html
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
| **Range**<br>[0, 4] |
| **Default Value**<br>4 |

> Note: Parameter `MaxThreadsInOneTask` is available for  `BarcodeReaderTaskSetting`, `LabelRecognizerTaskSetting` and `DocumentNormalizerTaskSetting`. They have the same parameter type, range and default value.
