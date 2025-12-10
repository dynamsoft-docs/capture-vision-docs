---
layout: default-layout
title: DeskewMode - Dynamsoft Document Normalizer Parameters
description: The parameter DeskewMode specifies the method to apply the deskew process on the target image.
keywords: DeskewMode
---

# DeskewMode

`DeskewMode` specifies the method in which the deskew process is applied to the target image. It consists of one of the following candidate modes, each mode represents an implementation.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_DESKEW_IMAGE")
            └── DeskewMode
```

**Parent object:** [DeskewImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-deskew-image.html)

**Example:**

```json
{
    "DeskewMode": {
        "ContentDirection": 0,
        "Mode": "DSM_PERSPECTIVE_CORRECTION"
    }
}
```

> [!NOTE]
> - This snippet shows only the `DeskewMode` parameter.
> - To use it, embed this parameter within a [DeskewImageStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-deskew-image.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

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
        <td><b>Candidate Mode List</b><br><br><a href = "#dsmperspectivecorrection">DSM_PERSPECTIVE_CORRECTION</a>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>["DSM_PERSPECTIVE_CORRECTION"]
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
        <td><b>Remarks</b><br>Only available for "DSM_PERSPECTIVE_CORRECTION".
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
        "Mode" : "DSM_PERSPECTIVE_CORRECTION"
    }
}
```

## Candidate Mode Introductions

### DSM_PERSPECTIVE_CORRECTION

Deskew the document by applying perspective correction process.
