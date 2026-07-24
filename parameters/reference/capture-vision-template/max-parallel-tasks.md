---
layout: default-layout
title: MaxParallelTasks - Dynamsoft Capture Vision Parameters
description: The parameter MaxParallelTasks defines the maximum number of parallel tasks for the DCV runtime.
keywords: Max parallel tasks, CaptureVisionTemplate
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
| **Remarks** <br>Controls the total number of concurrent thread slots used by the CVR thread pool. |

## Behavior

- Each DLR/DDN task occupies one thread slot.
- For DBR tasks, each localization work and each decoding work occupies one thread slot.
- When `MaxParallelTasks <= 1`, DBR runs in single-threaded mode.

In single-threaded mode for DBR, processing is executed in sequence:

1. Complete one `LocalizationMode` and produce localized barcode regions.
2. Apply all configured `DeblurMode`s to each localized barcode region.
3. Continue with the next `LocalizationMode`.


**Remarks**

- Updated semantic definition from "maximum parallel tasks" to "maximum concurrent thread slots in the CVR thread pool" in version 3.6.1000.
