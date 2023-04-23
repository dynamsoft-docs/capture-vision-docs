---
layout: default-layout
Title: CharacterNormalizationModes - Dynamsoft Label Recognizer Parameters
Description: The parameter CharacterNormalizationModes of Dynamsoft Label Recognizer defines how to normalize the characters.
Keywords: Character normalization
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/text-line-specification/character-model-name.html
---

# CharacterNormalizationModes

Parameter `CharacterNormalizationMode` defines an array of character normalization mode to implement. The array index represents the priority of the item. The smaller index is, the higher priority is.

## Example

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

## Parameter Summary

Parameter `CharacterNormalizationModes` consist of a group of character normalization mode objects. Each character normalization mode object includes a candidate mode and a series of mode arguments. The mode arguments of the character normalization mode object is shown as follow:

### Mode Arguments

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>
            Specifies a mode for character normalization.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br>
            String
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b>
                <br>CNM_MORPH
                <br>CNM_AUTO
                <br>CNM_SKIP
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
            ["CNM_SKIP"]
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">MorphOperation<br>(Optional)</td>
        <td><b>Description</b><br>
            Sets the morph operation.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br>
            String
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>"Erode", "Dilate", "Open" or "Close"
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
            "Close"
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>
            "Erode": Perform erosion process.<br>
            "Dilate": Perform dilation process.<br>
            "Open": Perform erosion first, then perform dilation.<br>
            "Close": Perform dilation first, then perform erosion.
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">MorphArgument<br>(Optional)</td>
        <td><b>Description</b><br>
            Sets the Argument ContentDirection.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br>
            int
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>
            [0,2]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
            0
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>
            Only available for "DM_PERSPECTIVE_CORRECTION".<br>
            0: Direction unknown.<br>
            1: Vertical direction.<br>
            2: Horizontal direction.
        </td>
    </tr>
</table>

### Default Setting

## Candidate Modes Introduction

### CNM_MORPH

Implement morphological transformations to normalize the characters.

### CNM_AUTO

Lets the library choose a mode automatically.
