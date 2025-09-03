---
layout: default-layout
title: ConfusableCharactersPath - Dynamsoft Label Recognizer Parameters
description: The parameter ConfusableCharactersPath of Dynamsoft Label Recognizer defines the path to the .data file of the confusable characters.
keywords: confusable characters path
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# ConfusableCharactersPath

The parameter `ConfusableCharactersPath` sets the path to the .data file of the confusable characters.

## Example

```json
{
    "ConfusableCharactersPath" : "D:\\YourApp\\ConfusableChars.data"
}
```

## Parameter Summary

| ConfusableCharactersPath Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The absolute file path or the path relative to the Dynamsoft Label Recognizer library.|
| **Default Value**<br>"" |
| **Remarks**<br>"" indicates that the confusable characters telling is not enabled. It works together with the [ConfusableCharactersCorrection](../text-line-specification/confusable-characters-correction.md) parameter to perform confusable characters correction during the recognition process.|
