---
layout: default-layout
Title: DeblurModes - Dynamsoft Barcode Reader Parameters
Description: The parameter DeblurModes of Dynamsoft Barcode Reader defines the mode and priority for deblurring.
Keywords: Deblur modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/deblur-modes.html
---

# DeblurModes

Parameter `DeblurModes` defines the mode and priority for deblurring.

## Example

```json
{
    "DeblurModes":
    [
        {
            "Mode": "DM_BASED_ON_LOC_BIN"
        },
        {
            "Mode": "DM_THRESHOLD_BINARIZATION" 
        }
    ]
}
```

## Parameter Summary

Parameter `DeblurModes` consist of a group of deblur mode objects. Each deblur mode object includes a candidate mode and a series of auxiliary mode arguments.

### Mode Arguments

The mode arguments of the deblur mode object are shown as follow:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Specifies a deblur mode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b>
            <br>DM_DIRECT_BINARIZATION
            <br>DM_THRESHOLD_BINARIZATION
            <br>DM_GRAY_EQUALIZATION
            <br>DM_SMOOTHING
            <br>DM_MORPHING
            <br>DM_DEEP_ANALYSIS
            <br>DM_SHARPENING
            <br>DM_BASED_ON_LOC_BIN
            <br>DM_SHARPENING_SMOOTHING
            <br>DM_SKIP
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LibraryFileName<br>(Optional)</td>
        <td><b>Description</b><br>Sets the file name of the library to load dynamically.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing file name.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes.
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LibraryParameters<br>(Optional)</td>
        <td><b>Description</b><br>The library must be in the same place with Dynamsoft Barcode Reader Library.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing parameters.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes.
        </td>
    </tr>
</table>

### Default Setting

## Candidate Modes Introduction

### DM_DIRECT_BINARIZATION

Performs deblur process using the binarization algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### DM_THRESHOLD_BINARIZATION

Performs deblur process using the threshold binarization algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### DM_GRAY_EQUALIZATION

Performs deblur process using the gray equalization algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### DM_SMOOTHING

Performs deblur process using the smoothing algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### DM_MORPHING

Performs deblur process using the morphing algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### DM_DEEP_ANALYSIS

Performs deblur process using the deep analysis algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### DM_SHARPENING

Performs deblur process using the sharpening algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### DM_BASED_ON_LOC_BIN

Performs deblur process based on the binary image from the localization process. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### DM_SHARPENING_SMOOTHING

Performs deblur process using the sharpening and smoothing algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters
