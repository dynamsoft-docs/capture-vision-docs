---
layout: default-layout
title: AssembleTextLinesStage - Dynamsoft Label Recognizer Parameters
description: The parameter defines Assemble Text Lines Stage under the Text Line Recognition Section.
keywords: Assemble Text Lines Stage
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# AssembleTextLinesStage Object

The `AssembleTextLinesStage` is designed at the stage level to assemble the grouped text-lines into a single text-line.

```json
{
    "Stage": "SST_ASSEMBLE_TEXT_LINES",
    "StringLengthRange": [
        3,
        200
    ],
    "StringRegExPattern": ""
}
```

## Stage

The stage is named `SST_ASSEMBLE_TEXT_LINES`.

## StringLengthRange

Parameter [`StringLengthRange`](string-length-range.md) sets the range of string lengths for concatenated strings of recognized text lines.

## StringRegExPattern

Parameter [`StringRegExPattern`](string-regex-pattern.md) specifies the regular expression pattern for concatenated strings of recognized text lines.
