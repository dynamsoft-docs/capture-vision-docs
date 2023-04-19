---
layout: default-layout
Title: BarcodeColourModes - Dynamsoft Barcode Reader Parameters
Description: The parameter BarcodeColourModes of Dynamsoft Barcode Reader defines the barcode colour modes.
Keywords: Barcode colour modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/barcode-colour-modes.html
---

# BarcodeColourModes

Parameter `BarcodeColourModes` defines the barcode colour modes. It consists of one or more modes, with each representing a different colour environment.

## Example

```json
"BarcodeColourModes" : 
[
    {
        "LightReflection" : 1,
        "Mode" : "BICM_DARK_ON_LIGHT"
    }
]
```

## Parameter Summary

Parameter `BarcodeColourModes` consist of a group of barcode colour mode objects. Each barcode colour mode object includes a candidate mode and a series of auxiliary parameters.

### Child Parameters

The child parameters of the barcode colour mode object are shown as follow:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Specifies a target barcode colour mode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>BICM_DARK_ON_LIGHT
            <br>BICM_LIGHT_ON_DARK
            <br>BICM_DARK_ON_DARK
            <br>BICM_LIGHT_ON_LIGHT
            <br>BICM_DARK_LIGHT_MIXED
            <br>BICM_DARK_ON_LIGHT_DARK_SURROUNDING
            <br>BICM_SKIP
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>BICM_DARK_ON_LIGHT
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LightReflection<br>(Optional)</td>
        <td><b>Description</b><br>A number from value range of LightReflection.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,1]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>1
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>0: no light reflection.
            <br>1: has light reflection.
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

The default settings of BarcodeColourModes is:

```json
{
    "BarcodeColourModes" : [
        {
            "LibraryFileName" : "",
            "LibraryParameters" : "",
            "LightReflection" : 1,
            "Mode" : "BICM_DARK_ON_LIGHT"
        }
    ],
}
```

## Candidate Modes Introduction

### BICM_DARK_ON_LIGHT

The target barcode is a dark item on a light background. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- LightReflection
- LibraryFileName
- LibraryParameters

### BICM_DARK_ON_LIGHT_DARK_SURROUNDING

The target barcode is a dark item on a light background surrounded by dark. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- LightReflection
- LibraryFileName
- LibraryParameters

### BICM_LIGHT_ON_DARK

The target barcode is a light item on a dark background. Not supported yet.

### BICM_DARK_ON_DARK

The target barcode is a dark item on a dark background. Not supported yet.

### BICM_LIGHT_ON_LIGHT

The target barcode is a light item on a light background. Not supported yet.

### BICM_DARK_LIGHT_MIXED

The target barcode is on background which is mixed by dark and light. Not supported yet