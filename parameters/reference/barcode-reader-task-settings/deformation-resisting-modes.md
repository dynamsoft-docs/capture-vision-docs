---
layout: default-layout
Title: DeformationResistingModes - Dynamsoft Barcode Reader Parameters
Description: The parameter DeformationResistingModes of Dynamsoft Barcode Reader defines how to handle distorted and deformed barcodes.
Keywords: Deblur modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/deformation-resisting-modes.html
---

# DeformationResistingModes

Parameter `DeformationResistingModes` defines how to handle distorted and deformed barcodes.

## Example

```json
{
    "DeformationResistingModes" :
    [
        {
            "Mode" : "DRM_SKIP"
        }
    ]
}
```

## Parameter Summary

Parameter `DeformationResistingModes` consist of a group of deformation resisting mode objects. Each deformation resisting mode object includes a candidate mode and a series of auxiliary mode arguments.

### Mode Arguments

The mode arguments of the deformation resisting mode object are shown as follow:

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Specifies a mode for deformation resisting.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>DRM_GENERAL
            <br>DRM_BROAD_WARP
            <br>DRM_LOCAL_REFERENCE
            <br>DRM_DEWRINKLE
            <br>DRM_AUTO
            <br>DRM_SKIP
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Level<br>(Optional)</td>
        <td><b>Description</b><br>Sets the Argument Level.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[1,9]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>5
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">GrayscaleEnhancementMode<br>(Optional)</td>
        <td><b>Description</b><br>Sets the Argument GrayscaleEnhancementMode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>GrayScaleEnhancementMode object</i>
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>View <a href="../image-parameter/grayscale-enhancement-modes.md">GrayScaleEnhancementModes</a> page for how to set this mode.
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">BinarizationMode<br>(Optional)</td>
        <td><b>Description</b><br>Sets the Argument BinarizationMode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>BinarizationMode object</i>
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>View <a href="../image-parameter/binarization-modes.md">BinarizationMode</a> page for how to set this parameter.
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

```json
"DeformationResistingModes" : 
[
    {
        "Mode" : "DRM_SKIP"
    }
]
```

## Candidate Modes Introduction

### DRM_GENERAL

Resists deformation using the general algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- Level
- LibraryFileName
- LibraryParameters

### DRM_BROAD_WARP

Resists deformation when the barcode is warped gently. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- BinarizationMode
- GrayscaleEnhancementMode

### DRM_LOCAL_REFERENCE

Resists deformation for barcodes with minor deformation in local modules. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- BinarizationMode
- GrayscaleEnhancementMode

### DRM_DEWRINKLE

Resists deformation for barcodes on a wrinkled surface. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- BinarizationMode
- GrayscaleEnhancementMode

### DRM_AUTO

Lets the library choose a mode automatically.
