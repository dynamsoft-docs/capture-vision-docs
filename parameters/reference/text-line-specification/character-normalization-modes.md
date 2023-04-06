---
layout: default-layout
Title: CharacterNormalizationModes - Dynamsoft Label Recognizer Parameters
Description: The parameter CharacterNormalizationModes of Dynamsoft Label Recognizer defines how to normalize the characters.
Keywords: Character normalization
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CharacterNormalizationModes

An array of `CharacterNormalizationMode` object that defines which mode to implement. The array index represents the priority of the item. The smaller index is, the higher priority is.

```json
{
    "CharacterNormalizationModes": 
    [
        {
            "Mode": "CNM_MORPH",
            "MorphOperation": "Close",
            "MorphArgument": "3",
        },
        {
            "Mode": "CNM_SKIP"
        }
    ]
}
```

|  |  |
| :------------------- | :------------------------ |
| Parameter Name | CharacterNormalizationModes |
| **Type** | *String* |
| Range | A object that defines with "CNM_MORPH", "CNM_AUTO" or "CNM_SKIP" |
| Default Value | "NumberLetter" |
