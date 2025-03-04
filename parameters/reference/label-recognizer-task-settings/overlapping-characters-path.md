---
layout: default-layout
title: OverlappingCharactersPath - Dynamsoft Label Recognizer Parameters
description: The parameter OverlappingCharactersPath of Dynamsoft Label Recognizer defines the path to the .data file containing characters features for overlapping matching.
keywords: characters overlapping matching
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# OverlappingCharactersPath

The parameter `OverlappingCharactersPath` sets the path to the .data file containing characters features for overlapping matching.

## Example

```json
{
    "OverlappingCharactersPath" : "D:\\YourApp\\OverlappingChars.data"
}
```

## Parameter Summary

| OverlappingCharactersPath Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The absolute file path or the path relative to the Dynamsoft Label Recognizer library.|
| **Default Value**<br>"" |
| **Remarks**<br>"" indicates that the characters overlapping matching is not enabled. |
