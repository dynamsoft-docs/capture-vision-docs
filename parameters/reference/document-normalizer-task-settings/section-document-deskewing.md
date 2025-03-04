---
layout: default-layout
title: Document Deskewing Section - Dynamsoft Document Normalizer Parameters
description: The parameter defines document deskewing section under the DocumentNormalizerTask.
keywords: Document Deskewing Section
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Document Deskewing Section

The Document Deskewing Section is designed to detect the edges of a document.

```json
{
    "Section": "ST_DOCUMENT_DESKEWING",
    "ImageParameterName": "ip_ddnDefault",
    "StageArray": []
}
```

## Section

The section is named `ST_DOCUMENT_DESKEWING`.

## ImageParameterName

Specifies the `ImageParameter` to apply in the stages of this section.

| Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>*It must be one of the name that defined under `ImageParameterOptions`* |
| **Default Value**<br>*ip_ddnDefault* |

## StageArray

`StageArray` is a parameter that specifies the stages within the `Document Deskewing Section`. A `Stage` is the smallest step significant enough to involve users in image processing.

The `Document Deskewing Section` consists of only one stage:

* [SST_DESKEW_IMAGE](./stage-deskew-image.md)
  * It is designed at the stage level to de-skew the quadrilateral to transform it into a rectangle.
