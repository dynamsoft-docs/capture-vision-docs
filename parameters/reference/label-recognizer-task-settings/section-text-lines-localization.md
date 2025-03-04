---
layout: default-layout
title: TextLinesLocalizationSection - Dynamsoft Label Recognizer Parameters
description: The parameter defines text lines localization section under the Section Array.
keywords: Text Lines Localization Section
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# TextLinesLocalizationSection Object

The `TextLinesLocalizationSection` is designed to detect the exact locations of text-lines.

```json
{
    "Section": "ST_TEXT_LINE_LOCALIZATION",
    "ImageParameterName": "ip_dlrDefault",
    "StageArray": []
}
```

## Section

The section is named `ST_TEXT_LINE_LOCALIZATION`.

## ImageParameterName

Specifies the `ImageParameter` to apply in the stages of this section.

| Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>*It must be one of the name that defined under `ImageParameterOptions`* |
| **Default Value**<br>*ip_dlrDefault* |

## StageArray

`StageArray` is a parameter that specifies the stages within the `TextLinesLocalizationSection`. A `Stage` is the smallest step significant enough to involve users in image processing.

The `TextLinesLocalizationSection` consists of a single stage:

* [SST_LOCALIZE_TEXT_LINES](stage-localize-text-lines.md)
  * It is designed at the stage level to detect the exact locations of text-lines.
