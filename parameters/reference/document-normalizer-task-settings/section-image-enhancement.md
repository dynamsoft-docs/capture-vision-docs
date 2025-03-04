---
layout: default-layout
title: Image Enhancement Section - Dynamsoft Document Normalizer Parameters
description: The parameter defines Image Enhancement section under the DocumentNormalizerTask.
keywords: Image Enhancement Section
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Image Enhancement Section

The Image Enhancement Section is designed to adjust the image quality.

```json
{
    "Section": "ST_IMAGE_ENHANCEMENT",
    "ImageParameterName": "ip_ddnDefault",
    "StageArray": []
}
```

## Section

The section is named `ST_IMAGE_ENHANCEMENT`.

## ImageParameterName

Specifies the `ImageParameter` to apply in the stages of this section.

| Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>*It must be one of the name that defined under `ImageParameterOptions`* |
| **Default Value**<br>*ip_ddnDefault* |

## StageArray

`StageArray` is a parameter that specifies the stages within the `Image Enhancement Section`. A `Stage` is the smallest step significant enough to involve users in image processing.

The `Image Enhancement Section` consists of only one stage:

* [SST_ENHANCE_IMAGE](./stage-enhance-image.md)
  * It is designed at the stage level to adjust the image quality, such as changing the brightness, contrast, and the color mode of the image.
