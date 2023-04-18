---
layout: default-layout
Title: DictionaryPath - Dynamsoft Label Recognizer Parameters
Description: The parameter DictionaryPath of Dynamsoft Label Recognizer defines the path of the dictionary file
Keywords: user dictionary, text correction
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DictionaryPath

Sets the path of the dictionary file.

```json
{
    "DictionaryPath" : "D:\\DictModel\\nutrition.txt"
}
```

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>The absolute file path.|
| **Default Value**<br>"" |
| **Remarks**<br>" " indicates that the dictionary is not enabled. It works together with the [DictionaryCorrectionThresholds](dictionary-correction-thresholds.md) parameter to perform error correction during the recognition process.|
