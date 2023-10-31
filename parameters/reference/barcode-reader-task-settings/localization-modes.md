---
layout: default-layout
title: LocalizationModes - Dynamsoft Barcode Reader Parameters
description: The parameter LocalizationModes of Dynamsoft Barcode Reader defines the line numers of the targeting text lines.
keywords: Localization modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/localization-modes.html
---

# LocalizationModes

Determines how to localize barcodes. It consists of one or more modes, each mode representing a different localization process. Different localization modes should be used depending on the targeted barcode format - for more info please see [Localization Modes Descriptions](#localization-modes-descriptions).

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
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
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
            LM_STATISTICS<br>
            LM_LINES<br>
            LM_SCAN_DIRECTLY<br>
            LM_STATISTICS_MARKS<br>
            LM_STATISTICS_POSTAL_CODE<br>
            LM_CENTRE<br>
            LM_ONED_FAST_SCAN<br>
            LM_SKIP<br>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
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
        <td><b>Valid For</b><br>All candidate modes.
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
        <td><b>Valid For</b><br>All candidate modes.
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

## Localization Modes Descriptions

### LM_CONNECTED_BLOCKS

Localizes barcodes by searching for connected blocks. This algorithm usually gives best result and it is recommended to set ConnectedBlocks to the highest priority no matter which barcode format you are scanning. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### LM_STATISTICS

Localizes barcodes by groups of contiguous black-white regions. This is optimized for QRCode and DataMatrix. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### LM_LINES

Localizes barcodes by searching for groups of lines. This is optimized for 1D and PDF417 barcodes. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### LM_SCAN_DIRECTLY

Localizes barcodes quickly. This mode is recommended in interactive scenario. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ScanStride
- ScanDirection
- IsOneDStacked
- LibraryFileName
- LibraryParameters

### LM_STATISTICS_MARKS

Localizes barcodes by groups of marks. This is optimized for DPM codes. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### LM_STATISTICS_POSTAL_CODE

Localizes barcodes by groups of connected blocks and lines.This is optimized for postal codes. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- LibraryFileName
- LibraryParameters

### LM_CENTRE

Localizes barcodes from the centre of the image. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ModuleSize
- LibraryFileName
- LibraryParameters

### LM_ONED_FAST_SCAN

Localizes 1D barcodes in a fast mode. This mode is designed for reading 1D barcodes in a very fast mode. This mode has the following arguments for further cuztomization.

**Available Mode Arguments:**

- ScanStride
- ScanDirection
- ConfidenceThreshold
- LibraryFileName
- LibraryParameters
