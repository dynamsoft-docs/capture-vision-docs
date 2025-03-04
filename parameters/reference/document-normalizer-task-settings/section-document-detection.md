---
layout: default-layout
title: Document Detection Section - Dynamsoft Document Normalizer Parameters
description: The parameter defines document detection section under the DocumentNormalizerTask.
keywords: Document Detection Section
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Document Detection Section

The Document Detection Section is designed to detect the edges of a document.

```json
{
    "Section": "ST_DOCUMENT_DETECTION",
    "ImageParameterName": "ip_ddnDefault",
    "StageArray": []
}
```

## Section

The section is named `ST_DOCUMENT_DETECTION`.

## ImageParameterName

Specifies the `ImageParameter` to apply in the stages of this section.

| Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>*It must be one of the name that defined under `ImageParameterOptions`* |
| **Default Value**<br>*ip_ddnDefault* |

## StageArray

`StageArray` is a parameter that specifies the stages within the `Document Detection Section`. A `Stage` is the smallest step significant enough to involve users in image processing.

The `Document Detection Section` consists of stages show below:

* [SST_ASSEMBLE_LONG_LINES](./stage-assemble-long-lines.md)
  * It is designed at the stage level to assemble relatively long line segments to facilitate the assembly of more advanced line segments.
* [SST_ASSEMBLE_LOGICAL_LINES](./stage-assemble-logical-lines.md)
  * It is designed at the stage level to assemble line segments based on certain criteria to serve the assembly of quadrilateral corners.
* [SST_DETECT_CORNERS](./stage-detect-corners.md)
  * It is designed at the stage level to detect corners of quadrilaterals that meet the specified conditions.
* [SST_DETECT_EDGES](./stage-detect-edges.md)
  * It is designed at the stage level to detect edges of quadrilaterals that meet the specified conditions.
* [SST_DETECT_QUADS](./stage-detect-quads.md)
  * It is designed at the stage level to detect complete quadrilaterals.
