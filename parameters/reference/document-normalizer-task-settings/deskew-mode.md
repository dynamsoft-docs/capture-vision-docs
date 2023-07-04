---
layout: default-layout
Title: DeskewMode - Dynamsoft Document Normalizer Parameters
Description: The parameter DeskewMode of Dynamsoft Document Normalizer is XXX.
Keywords:
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/document-normalizer-task-settings/deskew-mode.html
---

# DeskewMode

Parameter `DeskewMode` specifies the method in which the deskew process way used to apply the deskew process on the target normalized image. It consisits one of one following candidate modes, each mode represents an implement.

## Example

```json
{
    "DeskewMode" : 
    {
        "ContentDirection" : 0,
        "Mode" : "DM_PERSPECTIVE_CORRECTION"
    },
}
```

## Parameter Summary

DeskewMode is defined with a object that contains two mode arguments, `Mode` and `ContentDirection`.

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
        <td><b>Description</b><br>Specifies a mode for deskewing.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br><br><a href = "#dmperspectivecorrection">DM_PERSPECTIVE_CORRECTION</a>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>["DM_PERSPECTIVE_CORRECTION"]
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ContentDirection<br>(Optional)</td>
        <td><b>Description</b><br>Sets the Argument ContentDirection.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,2]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Only available for "DM_PERSPECTIVE_CORRECTION".
            <br>0: Direction unknown.
            <br>1: Vertical direction.
            <br>2: Horizontal direction.
        </td>
    </tr>
</table>

### Default Setting

If the `DeskewMode` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "DeskewMode" : 
    {
        "ContentDirection" : 0,
        "Mode" : "DM_PERSPECTIVE_CORRECTION"
    }
}
```

## Candidate Modes Introduction

### DM_PERSPECTIVE_CORRECTION

Deskew the document by applying perspective correction process.
