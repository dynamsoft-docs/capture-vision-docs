---
layout: default-layout
title: BarcodeComplementModes - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeComplementModes of Dynamsoft Barcode Reader defines how to complement the missing parts of a barcode.
keywords: Barcode complement modes
---

# BarcodeComplementModes

Parameter `BarcodeComplementModes` defines how to complement the missing parts of a barcode.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    ├── SectionArray[j]
    │   └── StageArray[k] (Stage object)
    │       └── BarcodeComplementModes
```

**Parent object:** [ComplementBarcodeStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-complement-barcode.html) object

**Example:**

```json
{
    "BarcodeComplementModes": [
        {
            "Mode": "BCM_GENERAL" 
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `BarcodeComplementModes` parameter.
> - To use it, embed this parameter within a complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

Parameter `BarcodeComplementModes` consists of a group of barcode complement mode objects. Each barcode complement mode object includes a candidate mode and a series of auxiliary mode arguments.

### Mode Arguments

The mode arguments of the barcode complement mode object are shown as follows:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Mode<br>(Required)</td>
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
</table>

### Default Setting

By default, barcode complement mode is not implemented.

```json
{
    "BarcodeComplementModes": [
        {
            "Mode": "BCM_SKIP"
        }
    ]
}
```

## Candidate Mode Introductions

### BCM_GENERAL

Complements the barcode using the general algorithm. This mode has the following arguments for further customization.

### BCM_AUTO

Lets the library choose a mode automatically. Not supported yet.
