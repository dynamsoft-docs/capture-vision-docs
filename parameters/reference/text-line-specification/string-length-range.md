---
layout: default-layout
title: StringLengthRange - Dynamsoft Capture Vision Text Line Specification Parameters
description: The parameter StringLengthRange of text line specification is for specifying the length range of the text line strings.
keywords: string length range, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# StringLengthRange

Sets the range of string length for each recognized line.

## Example

```json
{
    "StringLengthRange" : [3,50]
}
```

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int[]* |
| **Range**<br>The array contains only two elements, corresponding to the lower and upper bounds of the Range, respectively. The value range is [0, 0x7fffffff]. |
| **Default Value**<br>[3,50] |
| **Remarks**<br>An int array defines `MinValue` and `MaxValue` as the range of string length for each recognized line. Default values will be used if there is no manual setting. |
