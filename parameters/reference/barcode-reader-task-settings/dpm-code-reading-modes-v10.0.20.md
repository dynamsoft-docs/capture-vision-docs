---
layout: default-layout
title: DPMCodeReadingModes - Dynamsoft Barcode Reader Parameters
description: The parameter DPMCodeReadingModes of Dynamsoft Barcode Reader defines how to read direct part mark (DPM) barcodes.
keywords: DPM code reading modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DPMCodeReadingModes

Parameter `DPMCodeReadingModes` defines how to read direct part mark (DPM) barcodes.

## Example

```json
{
    "DPMCodeReadingModes":
    [
        {
            "Mode": "DPMCRM_GENERAL" 
        }
    ]
}
```

## Parameter Summary

Parameter `DPMCodeReadingModes` consist of a group of DPM code reading mode objects. Each object includes a candidate mode and a series of auxiliary mode arguments.

### Mode Arguments

The mode arguments of the DPM code reading mode object are shown as follow:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Specifies a mode to read DPM barcode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>DPMCRM_GENERAL
            <br>DPMCRM_AUTO
            <br>DPMCRM_SKIP
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

If the `DPMCodeReadingModes` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "DPMCodeReadingModes" : 
    [
        {
            "Mode" : "DPMCRM_SKIP"
        }
    ]
}
```

## Candidate Modes Introduction

### DPMCRM_GENERAL

Reads DPM codes using the general algorithm. This mode has the following arguments for further customizing.

- LibraryFileName
- LibraryParameters

### DPMCRM_AUTO

Lets the library choose a mode automatically. Not supported yet