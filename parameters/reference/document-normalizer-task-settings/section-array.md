---
layout: default-layout
title: SectionArray - Dynamsoft Document Normalizer Parameters
description: The parameter SectionArray defines which sections exist under the DocumentNormalizerTask.
keywords: Section Array parameter
---

# SectionArray

Parameter `SectionArray` defines which sections exist under the `DocumentNormalizerTask`. A `Section` is a sequence of `Stages` that form a relatively complete processing unit, producing milestone results that include location information along with other details.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray
```

**Parent object:** [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html) object

**Example:**

```json
{
    "SectionArray": [
        {
            "Section": "ST_REGION_PREDETECTION"
        },
        {
            "Section": "ST_DOCUMENT_DETECTION"
        },
        {
            "Section": "ST_DOCUMENT_DESKEWING"
        },
        {
            "Section": "ST_IMAGE_ENHANCEMENT"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `SectionArray` parameter.
> - To use it, embed this parameter within a [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The `DocumentNormalizerTask` includes the following sections:

* [RegionPredetectionSection](./section-regions-predetection.md) (`ST_REGION_PREDETECTION`)
  * Designed to find regions of interest (ROIs) and thus ignore other parts of the image during subsequent processing.
* [DocumentDetectionSection](./section-document-detection.md) (`ST_DOCUMENT_DETECTION`)
  * Designed to detect the edges of the document.
* [DocumentDeskewingSection](./section-document-deskewing.md) (`ST_DOCUMENT_DESKEWING`)
  * Designed to correct perspective distortion.
* [ImageEnhancementSection](./section-image-enhancement.md) (`ST_IMAGE_ENHANCEMENT`)
  * Designed to enhance the quality of the image.
