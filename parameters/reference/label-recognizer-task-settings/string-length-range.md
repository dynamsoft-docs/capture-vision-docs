---
layout: default-layout
Title: StringLengthRange - Dynamsoft Label Recognizer Parameters
Description: The parameter StringLengthRange of Dynamsoft Label Recognizer defines the range of string lengths for concatenated strings of recognized text lines.
Keywords: text lines, concatenated strings length
needAutoGenerateSidebar: true
noTitleIndex: true
---

# StringLengthRange

Sets the range of string lengths for concatenated strings of recognized text lines.

```json
{
    "StringLengthRange" : [3,200]
}
```

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int[]* |
| **Range**<br>The array contains only two elements, corresponding to the lower and upper bounds of the Range, respectively. The value range is [0, 0x7fffffff].|
| **Default Value**<br>[3,200] |
| **Remarks**<br>The first element is the lower bound and the second is the upper bound.|
