---
layout: default-layout
title: SectionArray - Dynamsoft Label Recognizer Parameters
description: The parameter SectionArray defines which sections exist under the LabelRecognizerTask.
keywords: Section Array parameter
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# SectionArray

`SectionArray` is a parameter that defines which sections exist under the `LabelRecognizerTask`. A `Section` is a sequence of Stages that form a relatively complete processing unit, producing milestone results that include location information along with other details.

The `LabelRecognizerTask` includes the following sections:

* [ST_REGION_PREDETECTION](section-regions-predetection.md)
  * It is designed to find regions of interest (ROIs) and thus ignoring other parts of the image during subsequent processing.
* [ST_TEXT_LINE_LOCALIZATION](section-text-lines-localization.md)
  * It is designed to detect the exact locations of text-lines.
* [ST_TEXT_LINE_RECOGNITION](section-text-lines-recognition.md)
  * It is designed to recognize the text from the text-line areas identified in the previous section [ST_TEXT_LINE_LOCALIZATION](text-line-localization-section.md)

```json
{
    "SectionArray":
    [
        {
            "Section": "ST_REGION_PREDETECTION",
            // Other parameters...
        },
        {
            "Section": "ST_TEXT_LINE_LOCALIZATION",
            // Other parameters...
        },
        {
            "Section": "ST_TEXT_LINE_RECOGNITION",
            // Other parameters...
        }
    ]
}
```
