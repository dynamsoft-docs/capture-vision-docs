---
layout: default-layout
title: MaxParallelTasks - Dynamsoft Capture Vision Parameters
description: The parameter MaxParallelTasks defines the maximum number of parallel tasks for the DCV runtime.
keywords: Max parallel tasks, CaptureVisionTemplate
permalink: /parameters/reference/capture-vision-template/max-parallel-tasks.html
---
# MaxParallelTasks

Parameter `MaxParallelTasks` defines the maximum number of parallel tasks for the DCV runtime.

## JSON Structure

**Location in template:**
```
CaptureVisionTemplates[i]
    └── MaxParallelTasks
```

**Parent object:** [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object

**Example:**

```json
{
    "MaxParallelTasks":4
}
```

> [!NOTE]
> - This snippet shows only the `MaxParallelTasks` parameter.
> - To use it, embed this parameter within a [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| MaxParallelTasks Parameter Details |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>-1, 0, [1, 256] |
| **Default Value**<br>4 |
| **Remarks** <br>1) 0: Only open the management thread, the execution task thread and the management thread are the same thread.<br>2) -1: Do not open the management thread or the task thread, that is, run in the thread that calls StartCapturing. |
