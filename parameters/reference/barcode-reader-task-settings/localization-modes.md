---
layout: default-layout
title: LocalizationModes - Dynamsoft Barcode Reader Parameters
description: The parameter LocalizationModes of Dynamsoft Barcode Reader defines how to localize barcodes.
keywords: Localization modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LocalizationModes

Determines how to localize barcodes. It consists of one or more modes, each mode representing a different localization process.

## Example

```json
"LocalizationModes" :
[
    {
        "Mode" : "LM_CONNECTED_BLOCKS"
    },
    {
        "Mode" : "LM_SCAN_DIRECTLY",
        "ScanDirection" : 0,
        "ScanStride" : 0
    }
]
```

## Parameter Summary

Parameter `LocalizationModes` consist of a group of localization mode objects. Each localization mode object includes a candidate mode and a series of auxiliary mode arguments. The structure of the localization mode object is shown as follow:

### Mode Arguments

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Any one in Candidate Mode List as string
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>
            LM_CONNECTED_BLOCKS<br>
            LM_LINES<br>
            LM_NEURAL_NETWORK<br>
            LM_SCAN_DIRECTLY<br>
            LM_STATISTICS<br>
            LM_STATISTICS_MARKS<br>
            LM_STATISTICS_POSTAL_CODE<br>
            LM_CENTRE<br>
            LM_ONED_FAST_SCAN<br>
            LM_SKIP<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ScanStride<br>(Optional)</td>
        <td><b>Description</b><br>Sets the stride in pixels between scans when searching for barcodes.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            LM_SCAN_DIRECTLY<br>
            LM_ONED_FAST_SCAN<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "6" style="vertical-align:text-top">ScanDirection<br>(Optional)</td>
        <td><b>Description</b><br>Sets the scan direction when searching barcode.
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
        <td><b>Remarks</b><br>0: Both vertical and horizontal direction.<br>1: Vertical direction.<br>2: Horizontal direction.
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            LM_SCAN_DIRECTLY<br>
            LM_ONED_FAST_SCAN<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ConfidenceThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the confidence threshold.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,100]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>60
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            LM_ONED_FAST_SCAN<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">IsOneDStacked<br>(Optional)</td>
        <td><b>Description</b><br>Sets whether the oned barcodes are stacked.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 1]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            LM_SCAN_DIRECTLY<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ModuleSize<br>(Optional)</td>
        <td><b>Description</b><br>Set the module size, if the module size is known.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            LM_CENTRE<br>
        </td>
    </tr>
    <tr>
        <td rowspan = "6" style="vertical-align:text-top">ModelNameArray<br>(Optional)</td>
        <td><b>Description</b><br>Sets the names of a barcode localization model.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String Array</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>Each element is the name of a model.<br>Candidate values: "OneDLocalization", "DataMatrixQRCodeLocalization".
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>null
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All candidate modes.
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Introduced in version 11.2.1000.<br>When set to null, both "OneDLocalization" and "DataMatrixQRCodeLocalization" models will be used by default.
        </td>
    </tr>
</table>

### Default Settings

If the `LocalizationModes` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "LocalizationModes" : 
    [
        {
            "Mode" : "LM_CONNECTED_BLOCKS"
        },
        {
            "IsOneDStacked" : 0,
            "Mode" : "LM_SCAN_DIRECTLY",
            "ScanDirection" : 0,
            "ScanStride" : 0
        },
        {
            "Mode" : "LM_STATISTICS",
        },
        {
            "Mode" : "LM_LINES",
        }
    ]
}
```

If you specified an localization mode object with Mode Argument "Mode" only, the default values of the other mode arguments will used.

## Candidate Modes Descriptions

### LM_CONNECTED_BLOCKS

Localizes barcodes by searching for connected blocks. This algorithm usually gives best result and it is recommended to set ConnectedBlocks to the highest priority. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ModelNameArray

### LM_STATISTICS

Localizes barcodes by groups of contiguous black-white regions. This is optimized for QRCode and DataMatrix. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ModelNameArray

### LM_LINES

Localizes barcodes by searching for groups of lines. This is optimized for 1D and PDF417 barcodes. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ModelNameArray

### LM_SCAN_DIRECTLY

Localizes barcodes quickly. This mode is recommended in interactive scenario. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ScanStride
- ScanDirection
- IsOneDStacked
- ModelNameArray

### LM_STATISTICS_MARKS

Localizes barcodes by groups of marks. This is optimized for DPM codes. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ModelNameArray

### LM_STATISTICS_POSTAL_CODE

Localizes barcodes by groups of connected blocks and lines.This is optimized for postal codes. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ModelNameArray

### LM_CENTRE

Localizes barcodes from the centre of the image. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ModuleSize
- ModelNameArray

### LM_ONED_FAST_SCAN

Localizes 1D barcodes in a fast mode. This mode is designed for reading 1D barcodes in a very fast mode. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ScanStride
- ScanDirection
- ConfidenceThreshold
- ModelNameArray

### LM_NEURAL_NETWORK

Localizes barcodes by utilizing a neural network model. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ModelNameArray

