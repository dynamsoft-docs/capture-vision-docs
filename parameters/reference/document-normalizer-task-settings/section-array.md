---
layout: default-layout
title: SectionArray - Dynamsoft Document Normalizer Parameters
description: The parameter SectionArray defines which sections exist under the DocumentNormalizerTask.
keywords: Section Array parameter
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# SectionArray

`SectionArray` is a parameter that defines which sections exist under the `DocumentNormalizerTask`. A `Section` is a sequence of Stages that form a relatively complete processing unit, producing milestone results that include location information along with other details.

The `DocumentNormalizerTask` includes the following sections:

* [ST_REGION_PREDETECTION](./section-regions-predetection.md)
  * It is designed to find regions of interest (ROIs) and thus ignoring other parts of the image during subsequent processing.
* [ST_DOCUMENT_DETECTION](./section-document-detection.md)
  * It is designed to detect the edges of the document.
* [ST_DOCUMENT_DESKEWING](./section-document-deskewing.md)
  * It is designed to correct perspective distortion.
* [ST_IMAGE_ENHANCEMENT](./section-image-enhancement.md)
  * It is designed to enhance the quality of the image.

```json
{
    "SectionArray":
    [
        {
            "Section": "ST_REGION_PREDETECTION",
            // Other parameters...
        },
        {
            "Section": "ST_DOCUMENT_DETECTION",
            // Other parameters...
        },
        {
            "Section": "ST_DOCUMENT_DESKEWING",
            // Other parameters...
        },
        {
            "Section": "ST_IMAGE_ENHANCEMENT",
            // Other parameters...
        }
    ]
}
```
