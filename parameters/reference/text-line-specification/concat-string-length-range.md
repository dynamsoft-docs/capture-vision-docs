---
layout: default-layout
title: ConcatStringLengthRange - Dynamsoft Label Recognizer Parameters
description: The parameter ConcatStringLengthRange of text line specification is for specifying the length range of the text line strings.
keywords: concat string length range, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ConcatStringLengthRange

Sets the range of string length for the concated recognized text lines.

## Example

```json
{
    "ConcatStringLengthRange" : [3,200]
}
```

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int[]* |
| **Range**<br>The array contains only two elements, corresponding to the lower and upper bounds of the Range, respectively. The value range is [3, 0x7fffffff]. |
| **Default Value**<br>[3,200] |
| **Remarks**<br>An int array defines `MinValue` and `MaxValue` as the range of string length for the concated recognized text lines. |
