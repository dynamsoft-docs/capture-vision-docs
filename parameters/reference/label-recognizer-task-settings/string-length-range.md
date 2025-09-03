---
layout: default-layout
title: StringLengthRange - Dynamsoft Label Recognizer Parameters
description: The parameter StringLengthRange of Dynamsoft Label Recognizer defines the range of string lengths for concatenated strings of recognized text lines.
keywords: text lines, concatenated strings length
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/label-recognizer-task-settings/string-length-range.html
---

# StringLengthRange

Parameter `StringLengthRange` sets the range of string lengths for concatenated strings of recognized text lines.

## Example

```json
{
    "StringLengthRange" : [3,200]
}
```

## Parameter Summary

| StringLengthRange Parameter Summary |
| :----------------------------------- |
| **Type**<br>*int[]* |
| **Range**<br>The array contains only two elements, corresponding to the lower and upper bounds of the Range, respectively. The value range is [0, 0x7fffffff].|
| **Default Value**<br>[3,200] |
| **Remarks**<br>The first element is the lower bound and the second is the upper bound.|
