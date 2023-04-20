---
layout: default-layout
Title: DictionaryCorrectionThresholds - Dynamsoft Label Recognizer Parameters
Description: The parameter DictionaryCorrectionThresholds of Dynamsoft Label Recognizer defines the threshold of dictionary error correction.
Keywords: user dictionary, text correction
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/label-recognizer-task-settings/dictionary-correction-thresholds.html
---

# DictionaryCorrectionThresholds

Sets the threshold of dictionary error correction.

## Example

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

## Parameter Summary

Parameter `DictionaryCorrectionThresholds` consist of a group of dictionary correction threshold objects. Each threshold object includes a series of child parameters.

### Child Parameter Summary

<table style = "text-align:left">
    <thead>
        <tr>
            <th>Child Parameter Name</th>
            <th>Child Parameter Summary</th>
        </tr>
    </thead>
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
            The maximum number of correctable characters per word.
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

### Default Setting

If the parameter `DictionaryCorrectionThresholds` is not included in your template file, the following setting will be used.

```json
{
    "DictionaryCorrectionThresholds" : 
    [
        {
            "MaxWordLength" : 256,
            "MinWordLength" : 3,
            "Threshold" : 1
        }
    ]
}
```

If any of `MaxWordLength`, `MinWordLength` or `Threshold` is missing in your dictionary correction threshold object, the default values of the child parameters will be used.
