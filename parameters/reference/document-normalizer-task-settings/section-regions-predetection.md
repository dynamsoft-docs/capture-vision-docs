---
layout: default-layout
title: Regions Predetection Section - Dynamsoft Label Recognizer Parameters
description: The parameter defines regions predtection section under the LabelRecognizerTask.
keywords: Regions Predetection Section
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Regions Predetection Section

The Regions Predetection Section is designed to identify regions of interest (ROIs), allowing subsequent processing to ignore other parts of the image. The pre-detected region may be identified based on color features, grayscale features, or neural network localization.

```json
{
    "Section": "ST_REGION_PREDETECTION",
    "ImageParameterName": "ip_dlrDefault",
    "StageArray": []
}
```

## Section

The section is named `ST_REGION_PREDETECTION`.

## ImageParameterName

Specifies the `ImageParameter` to apply in the stages of this section.

| Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>*It must be one of the name that defined under `ImageParameterOptions`* |
| **Default Value**<br>*ip_dlrDefault* |

## StageArray

`StageArray` is a parameter that specifies the stages within the `Regions Predetection Section`. A `Stage` is the smallest step significant enough to involve users in image processing.

The `Regions Predetection Section` consists of a single stage:

* [SST_PREDETECT_REGIONS](./stage-predetect-regions.md)
  * It is designed at the stage level to identify regions of interest (ROIs).
