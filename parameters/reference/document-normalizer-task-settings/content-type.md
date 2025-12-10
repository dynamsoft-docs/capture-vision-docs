---
layout: default-layout
title: ContentType - Dynamsoft Document Normalizer Parameters
description: The parameter ContentType defines which contents are the targeting objects.
keywords: ContentType
---

# ContentType

`ContentType` defines which contents are the targeting objects.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object where Section = "ST_DOCUMENT_DETECTION")
        └── ContentType
```

**Parent object:** [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html)

**Example:**

```json
{
    "ContentType": "CT_TABLE"
}
```

> [!NOTE]
> - This snippet shows only the `ContentType` parameter.
> - To use it, embed this parameter within a [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| ContentType Parameter Details |
| :---------------------------- |
| **Type**<br>*String* |
| **Available Content Type**<br><br>CT_DOCUMENT<br>CT_TABLE<br>CT_UNKNOWN |
| **Default Value**<br>"CT_DOCUMENT" |
