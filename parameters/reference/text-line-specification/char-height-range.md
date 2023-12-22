---
layout: default-layout
title: CharHeightRange - Dynamsoft Label Recognizer Parameters
description: The parameter CharHeightRange of Dynamsoft Label Recognizer defines the range of the character height.
keywords: Applicable text line numbers
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/text-line-specification/char-height-range.html
---

# CharHeightRange

Parameter `CharHeightRange` defines the range of the character height (in pixel or a percentage value relative to the height of the `targetROI`).

## Example

```json
{
    "CharHeightRange": [ 800, 1000, 1 ]
}
```

## Parameter Summary

| CharHeightRange Parameter Summary |
| :-------------------------------- |
| **Type**<br>*int Array* |
| **Range**<br>The third member should be 0 or 1, which determines whether the range is measured by thousandth. If measured by thousandth, the first 2 members should be int values between 1 to 1000. Otherwise, they should between 1 to 0x7fffffff. |
| **Default Value**<br>"" |
| **Remarks**<br>Format: [MinHeight, MaxHeight, ByThousandth]. |
