---
layout: default-layout
title: DeblurModes - Dynamsoft Barcode Reader Parameters
description: The parameter DeblurModes of Dynamsoft Barcode Reader defines the mode and priority for deblurring.
keywords: Deblur modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
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
            <br>DM_NEURAL_NETWORK
            <br>DM_SKIP
        </td>
    </tr>
    <tr>
        <td rowspan = "6" style="vertical-align:text-top">DeblurModelNameArray<br>(Optional)</td>
        <td><b>Description</b><br>Sets the Convolutional Neural Networks (CNN) model files used for barcode decoding. It references the names of <a href="{{ site.dcvb_parameters }}file/auxiliary/capture-vision-model.html" target="_blank">CaptureVisionModel</a> objects.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String Array</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>Each element is the name of a `CaptureVisionModel` object.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>DM_NEURAL_NETWORK.
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Deprecated in version 11.2.1000 and will be removed in future versions. Please use `ModelNameArray` instead.<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "6" style="vertical-align:text-top">ModelNameArray<br>(Optional)</td>
        <td><b>Description</b><br>Sets the Convolutional Neural Networks (CNN) model files used for barcode decoding. It references the names of <a href="{{ site.dcvb_parameters }}file/auxiliary/capture-vision-model.html" target="_blank">CaptureVisionModel</a> objects.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String Array</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>Each element is the name of a `CaptureVisionModel` object.<br>Candidate values: "OneDDeblur", "EAN13Decoder", "Code128Decoder".
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>DM_NEURAL_NETWORK.
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Introduced in version 11.2.1000.<br>When set to null, all "OneDDeblur", "EAN13Decoder", "Code128Decoder" models will be used by default.
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Level<br>(Optional)</td>
        <td><b>Description</b><br>Sets the effort level used for deblurring, a larger value may improve the Read Rate but slowdown the Speed.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[1, 9]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>4
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>DM_NEURAL_NETWORK.
        </td>
    </tr>
    <tr>
        <td rowspan = "6" style="vertical-align:text-top">Methods<br>(Optional)</td>
        <td><b>Description</b><br>Sets the methods used for deep analysis.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String Array</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>Each element is a deep analysis method.<br>OneDGeneral: for OneD barcodes.<br>TwoDGeneral: for 2D barcodes.<br>EAN13Enhanced: for EAN13 barcodes.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>DM_DEEP_ANALYSIS.
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Introduced in version 11.2.1000.<br>
        </td>
    </tr>
</table>

### Default Setting

If the `DeblurModes` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "DeblurModes": null
}
```

**Remarks**  

The actual deblur modes used are:
- For Barcode Format PDF417

[DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_SMOOTHING,DM_GRAY_EQUALIZATION,DM_MORPHING,DM_DEEP_ANALYSIS]

- For Barcode Format OneD  

[DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,**DM_NEURAL_NETWORK(with EAN13Decoder and Code128Decoder)**,DM_DEEP_ANALYSIS,DM_SMOOTHING,DM_GRAY_EQUALIZATION,DM_MORPHING]

- For other formats

[DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_DEEP_ANALYSIS,DM_SMOOTHING,DM_GRAY_EQUALIZATION,DM_MORPHING]

## Candidate Modes Introduction

### DM_DIRECT_BINARIZATION

Performs deblur process using the binarization algorithm. This mode has the following arguments for further customizing.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### DM_THRESHOLD_BINARIZATION

Performs deblur process using the threshold binarization algorithm.

When processing OneD barcodes, you can add two `DM_THRESHOLD_BINARIZATION` to your DeblurModes settings. If you do, the second round `DM_THRESHOLD_BINARIZATION` will detect and fill in the blurry area with predicted barcode modules. The second round `DM_THRESHOLD_BINARIZATION` can sharpenly improve the read-rate of blurry OneD barcodes but sacrifice the accuracy.

This mode has the following arguments for further customizing.

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


### DM_NEURAL_NETWORK

Performs deblur process by utilizing a neural network model.

**Available Mode Arguments:**

- ModelNameArray
- Level
- LibraryFileName
- LibraryParameters
