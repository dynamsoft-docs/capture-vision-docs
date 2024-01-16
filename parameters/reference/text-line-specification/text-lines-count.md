---
layout: default-layout
title: TextLinesCount - Dynamsoft Label Recognizer Parameters
description: The parameter TextLinesCount defines the expected number of text lines for the TextLineSpecification object.
keywords: TextLinesCount
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/text-line-specification/text-lines-count.html
---

# TextLinesCount

Parameter `TextLinesCount` defines the expected number of text lines for the `TextLineSpecification` object.

## Example

```json
{
    "Name": "tls_0",
    "TextLinesCount" : 3
}
```

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br>0. It represents the total number of text lines in the group. |
