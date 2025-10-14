---
layout: default-layout
title: MaxParallelTasks - Dynamsoft Capture Vision Parameters
description: The parameter MaxParallelTasks defines the maximum number of parallel tasks for the DCV runtime.
keywords: Max parallel tasks, CaptureVisionTemplate
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/capture-vision-template/max-parallel-tasks.html
---

# MaxParallelTasks

Parameter `MaxParallelTasks` defines the maximum number of parallel tasks for the DCV runtime.

## Example

```json
{
    "MaxParallelTasks":4
}
```

## Parameter Summary

| MaxParallelTasks Parameter Summary |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>-1, 0, [1, 256] |
| **Default Value**<br>4 |
| **Remarks** <br>1) 0: Only open the management thread, the execution task thread and the management thread are the same thread.<br>2) -1: Do not open the management thread or the task thread, that is, run in the thread that calls StartCapturing. |
