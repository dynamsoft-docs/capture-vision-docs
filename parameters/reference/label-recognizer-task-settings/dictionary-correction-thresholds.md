---
layout: default-layout
Title: DictionaryCorrectionThresholds - Dynamsoft Label Recognizer Parameters
Description: The parameter DictionaryCorrectionThresholds of Dynamsoft Label Recognizer defines the threshold of dictionary error correction.
Keywords: user dictionary, text correction
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DictionaryCorrectionThresholds

Sets the threshold of dictionary error correction.

```json
{
    "DictionaryCorrectionThresholds": [
        {
            "MinWordLength": 3,
            "MaxWordLength": 5,
            "Threshold": 1
        },
        {
            "MinWordLength": 6,
            "MaxWordLength": 10,
            "Threshold": 2
        },
        {
            "MinWordLength": 11,
            "Threshold": 3
        }
    ]

}
```

**Remarks**

- It supports segmentation threshold.
- It works together with the [DictionaryPath](dictionary-path.md) parameter to perform error correction during the recognition process.

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">MinWordLength<br>(Required)</td>
        <td><b>Description</b><br>
            The minimum value of word length.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br>
            int
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>
            [0,0x7ffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
            3
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">MaxWordLength<br>(Required)</td>
        <td><b>Description</b><br>
            The maximum value of word length.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br>
            int
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>
            [0,0x7ffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
            256
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>
            MaxWordLength >= MinWordLength<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Threshold<br>(Required)</td>
        <td><b>Description</b><br>
            The threshold for the number of error correction characters.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br>
            int
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>
            [0,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
            1
        </td>
    </tr>
</table>
