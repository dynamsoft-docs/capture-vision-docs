---
layout: default-layout
title: MaxThreadsInOneTask - Dynamsoft Document Normalizer Parameters
description: The parameter MaxThreadsInOneTask defines the maximum threads that can be consumed in one document normalizer task.
keywords: Max threads
---

# MaxThreadsInOneTask

`MaxThreadsInOneTask` defines the maximum threads that can be consumed in one task.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── MaxThreadsInOneTask
```

**Parent object:** [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html)

**Example:**

```json
{
    "MaxThreadsInOneTask": 4
}
```

> [!NOTE]
> - This snippet shows only the `MaxThreadsInOneTask` parameter.
> - To use it, embed this parameter within a [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| MaxThreadsInOneTask Parameter Details |
| :------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 256] |
| **Default Value**<br>0 |

**Remarks**

- Changed the default value to 0 from 4 in version 3.2.1000
- Updated the value range to [0, 256] in version 3.2.1000.
