# CharacterNormalizationModes

Define how the characters will be normalized in the specified text line.

The quality of characters are not enough for recognition.

CharacterNormalizationModes is a parameter for setting the mode for character normalization. It consisits of one or more CharacterNormalizationMode items and each item has its own arguments. The array index represents the priority of the item. The smaller index is, the higher priority is.

```json
{
    "CharacterNormalizationModes": 
    [
        {
            "Mode": "CNM_MORPH",
            "MorphOperation": "Close",
            "MorphArgument": "3",
        }
    ]
}
```
