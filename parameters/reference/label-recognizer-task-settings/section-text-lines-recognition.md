---
layout: default-layout
title: TextLinesRecognitionSection - Dynamsoft Label Recognizer Parameters
description: The parameter defines text lines recognition section under the Section Array.
keywords: Text Lines Recognition  Section
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# TextLinesRecognitionSection Object

The `TextLinesRecognitionSection` is designed to detect the exact locations of text-lines.

```json
{
    "Section": "ST_TEXT_LINE_RECOGNITION",
    "ImageParameterName": "ip_dlrDefault",
    "StageArray": []
}
```

## Section

The section is named `ST_TEXT_LINE_RECOGNITION`.

## ImageParameterName

Specifies the `ImageParameter` to apply in the stages of this section.

| Parameter Summary |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>*It must be one of the name that defined under `ImageParameterOptions`* |
| **Default Value**<br>*ip_dlrDefault* |

## StageArray

`StageArray` is a parameter that specifies the stages within the `TextLinesRecognitionSection`. A `Stage` is the smallest step significant enough to involve users in image processing.

The `TextLinesRecognitionSection` consists of two stages:

* [SST_RECOGNIZE_RAW_TEXT_LINES](stage-recognize-raw-text-lines.md)
  * It is designed at the stage level to recognize the raw values of text-lines.
* [SST_ASSEMBLE_TEXT_LINES](stage-assemble-text-lines.md)
  * It is designed at the stage level to assemble the grouped text-lines into a single text-line.
