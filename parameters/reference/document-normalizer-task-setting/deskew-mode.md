---
layout: default-layout
Title: DeskewMode - Dynamsoft Document Normalizer Parameters
Description: The parameter DeskewMode of Dynamsoft Document Normalizer is XXX.
Keywords:
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DeskewMode

DeskewMode specifies the method in which the deskew process way used to apply the deskew process on the target normalized image. It consisits one of one following candidate modes, each mode represents an implement.

```json
{
    "DeskewMode" : 
    {
        "ContentDirection" : 0,
        "Mode" : "DM_PERSPECTIVE_CORRECTION"
    },
}
```

## Candidate Mode List

- [DM_PERSPECTIVE_CORRECTION](#dm_perspective_correction)

### DM_PERSPECTIVE_CORRECTION

Deskew the document by applying perspective correction process. This mode has the following arguments for further customizing.

## Definition Details

DeskewMode is defined with a object that contains two child parameters, `Mode` and `ContentDirection`.

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Details</th>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>
            Specifies a mode for deskewing.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br>
            String
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>
            Anyone in Candidate Mode List as a string.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
            ["DM_PERSPECTIVE_CORRECTION"]
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ContentDirection<br>(Optional)</td>
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
