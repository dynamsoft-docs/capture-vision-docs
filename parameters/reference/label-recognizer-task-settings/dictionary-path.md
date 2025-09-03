---
layout: default-layout
title: DictionaryPath - Dynamsoft Label Recognizer Parameters
description: The parameter DictionaryPath of Dynamsoft Label Recognizer defines the path of the dictionary file
keywords: user dictionary, text correction
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/label-recognizer-task-settings/dictionary-path.html
---

# DictionaryPath

Parameter `DictionaryPath` sets the path of the dictionary file.

## Example

```json
{
    "DictionaryPath" : "D:\\DictModel\\nutrition.txt"
}
```

## Parameter Summary

| DictionaryPath Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The absolute file path.|
| **Default Value**<br>"" |
| **Remarks**<br>" " indicates that the dictionary is not enabled. It works together with the [DictionaryCorrectionThresholds](dictionary-correction-thresholds.md) parameter to perform error correction during the recognition process.|
