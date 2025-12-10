---
layout: default-layout
title: DictionaryCorrectionThresholds - Dynamsoft Label Recognizer Parameters
description: The parameter DictionaryCorrectionThresholds of Dynamsoft Label Recognizer defines the threshold of dictionary error correction.
keywords: user dictionary, text correction
---

# DictionaryCorrectionThresholds

Parameter `DictionaryCorrectionThresholds` sets the threshold of dictionary error correction.

## JSON Structure

**Location in template:**

```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_RECOGNIZE_RAW_TEXT_LINES")
            └── DictionaryCorrectionThresholds
```

**Parent object:** [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html)

**Example:**

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

> [!NOTE]
> - This snippet shows only the `DictionaryCorrectionThresholds` parameter.
> - To use it, embed this parameter within a [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json)

**Remarks**

- It supports segmentation threshold.
- It works together with the [DictionaryPath](dictionary-path.md) parameter to perform error correction during the recognition process.

## Parameter Details

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
