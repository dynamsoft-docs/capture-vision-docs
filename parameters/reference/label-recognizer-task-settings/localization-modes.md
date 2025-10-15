---
layout: default-layout
title: LocalizationModes - Dynamsoft Label Recognizer Parameters
description: The parameter LocalizationModes of Dynamsoft Label Recognizer defines how to localize text lines.
keywords: Localization modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LocalizationModes

Determines how to localize barcodes. It consists of one or more modes, each mode representing a different localization process.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.2.1000.

## Example

```json
"LocalizationModes" :
[
    {
        "Mode" : "LM_NEURAL_NETWORK",
        "ModelNameArray": ["MRZLocalization"]
    },
    {
        "Mode" : "LM_GENERAL"
    }
]
```

## Parameter Summary

Parameter `LocalizationModes` consist of a group of localization mode objects. Each localization mode object includes a candidate mode and a series of auxiliary mode arguments. The structure of the localization mode object is shown as follow:

### Mode Arguments

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Any one in Candidate Mode List as string
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>
            LM_NEURAL_NETWORK<br>
            LM_GENERAL<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "6" style="vertical-align:text-top">ModelNameArray<br>(Optional)</td>
        <td><b>Description</b><br>Sets the names of a text localization model.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String Array</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>Each element is the name of a model. Candidate values: "MRZLocalization".
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>LM_NEURAL_NETWORK.
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>When set to null, model "MRZLocalization" will be used by default.
        </td>
    </tr>
</table>

### Default Settings

If the `LocalizationModes` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "LocalizationModes" : 
    [
        {
            "Mode" : "LM_GENERAL"
        }
    ]
}
```

## Candidate Modes Descriptions

### LM_GENERAL

Localizes text lines using general image processing algorithms.

### LM_NEURAL_NETWORK

Localizes text lines by utilizing a neural network model. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ModelNameArray

