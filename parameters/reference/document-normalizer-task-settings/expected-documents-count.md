---
layout: default-layout
title: ExpectedDocumentsCount - Dynamsoft Document Normalizer Parameters
description: The parameter ExpectedDocumentsCount sets the number of documents expected to be detected.
keywords: Expected Documents Count
---

# ExpectedDocumentsCount

`ExpectedDocumentsCount` sets the number of documents expected to be detected.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── ExpectedDocumentsCount
```

**Parent object:** [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html)

**Example:**

```json
{
    "ExpectedDocumentsCount": 1
}
```

> [!NOTE]
> - This snippet shows only the `ExpectedDocumentsCount` parameter.
> - To use it, embed this parameter within a [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| ExpectedDocumentsCount Parameter Details |
| :--------------- |
| **Type**<br><i>int</i> |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br> 1 |
