---
layout: default-layout
Title: BarcodeComplementModes - Dynamsoft Barcode Reader Parameters
Description: The parameter BarcodeComplementModes of Dynamsoft Barcode Reader defines the barcode colour modes.
Keywords: Barcode complement modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/barcode-complement-modes.html
---

## BarcodeComplementModes

Parameter `BarcodeComplementModes` defines how to complement the missing parts of a barcode.

## Example

```json
{
    "BarcodeComplementModes": [
        {
            "Mode": "BCM_GENERAL" 
        }
    ]
}
```

## Parameter Summary

Parameter `BarcodeComplementModes` consist of a group of barcode complement mode objects. Each barcode complement mode object includes a candidate mode and a series of auxiliary mode arguments.

### Mode Arguments

The mode arguments of the barcode complement mode object are shown as follow:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Specifies a barcode complement mode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>BCM_GENERAL
            <br>BCM_AUTO
            <br>BCM_SKIP
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>BCM_SKIP
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

### Default Settings

Barcode complement mode is not implemented by default

```json
{
    "BarcodeComplementModes" : 
    [
        {
        "Mode" : "BCM_SKIP"
        }
   ]
}
```

## Candidate Modes Introduction

### BCM_GENERAL

Complements the barcode using the general algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### BCM_AUTO

Lets the library choose a mode automatically. Not supported yet
