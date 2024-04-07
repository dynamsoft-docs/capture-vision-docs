---
layout: default-layout
title: ConfusableCharactersCorrection - Dynamsoft Label Recognizer Parameters
description: The parameter ConfusableCharactersCorrection of text line specification is for correcting the confusable characters.
keywords: confusable characters correction, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ConfusableCharactersCorrection

The parameter `ConfusableCharactersCorrection` defines the confusing character set and an array of reference font names for error correction.

The currently supported built-in fonts are as follows:

- ARIAL
- COURIER_NEW
- OCR_B
- TIMES_NEW_ROMAN
- VERDANA
- HELVETICA

The currently supported built-in confusable characters sets are as follows:

- ["0", "o", "O"]
- ["l", "1", "I"]
- ["5", "s", "S"]

## Example

```json
{
    "ConfusableCharactersCorrection": 
    {
        "ConfusableCharacters": [
            ["0", "o", "O"],
            ["l", "1", "I"],
            ["5", "s", "S"]
        ],
        "FontNameArray": [
            "ARIAL"
        ]
    }
}
```

## Parameter Summary

### ConfusableCharacters

Parameter `ConfusableCharacters` defines an array of confusing characters sets for correction.

| ConfusableCharacters Parameter Summary |
| :------------------- |
| **Type**<br>*String[][]* |
| **Range**<br>Each row of the array should be a supported confusing characters set. The currently supported built-in confusable characters sets are as follows:<br>["0", "o", "O"]<br>["l", "1", "I"]<br>["5", "s", "S"]|
| **Default Value**<br>[<br>  ["0", "o", "O"],<br>  ["l", "1", "I"],<br>  ["5", "s", "S"]<br>] |

### FontNameArray

Parameter `FontNameArray` is an array of supported font names.

| FontNameArray Parameter Summary |
| :------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each member should be a supported font name. The currently supported built-in fonts are as follows:<br>ARIAL<br>COURIER_NEW<br>OCR_B<br>TIMES_NEW_ROMAN<br>VERDANA<br>HELVETICA|
| **Default Value**<br>null |
| **Remarks**<br>null indicates that the confusable characters telling is not enabled. |
