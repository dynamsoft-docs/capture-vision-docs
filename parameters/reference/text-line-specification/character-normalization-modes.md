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

Candidate Mode List

- CNM_MORPH
- CNM_AUTO
- CNM_SKIP

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
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
