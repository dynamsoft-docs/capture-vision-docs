---
layout: default-layout
Title: LocalizationModes - Dynamsoft Barcode Reader Parameters
Description: The parameter LocalizationModes of Dynamsoft Barcode Reader defines the line numers of the targeting text lines.
Keywords: Localization modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LocalizationModes

LocalizationModes determines how to localize barcodes. It consists of one or more modes, each mode representing a different localization process.

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

Parameter `LocalizationModes` consist of a group of localizaion mode objects. Each localization mode object includes a candidate mode and a series of auxiliary parameters. The structure of the localization mode object is shown as follow:

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
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
            <li>LM_CONNECTED_BLOCKS</li>
            <li>LM_STATISTICS</li>
            <li>LM_LINES</li>
            <li>LM_SCAN_DIRECTLY</li>
            <li>LM_STATISTICS_MARKS</li>
            <li>LM_STATISTICS_POSTAL_CODE</li>
            <li>LM_CENTRE</li>
            <li>LM_ONED_FAST_SCAN</li>
            <li>LM_SKIP</li>
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
            <li>LM_SCAN_DIRECTLY</li>
            <li>LM_ONED_FAST_SCAN</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ScanDirection<br>(Optional)</td>
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
        <td><b>Valid For</b><br>
            <li>LM_SCAN_DIRECTLY</li>
            <li>LM_ONED_FAST_SCAN</li>
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
            <li>LM_ONED_FAST_SCAN</li>
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
            <li>LM_SCAN_DIRECTLY</li>
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

The default settings of LocalizationModes is:

```json
"LocalizationModes" : [
    {
        "LibraryFileName" : "",
        "LibraryParameters" : "",
        "Mode" : "LM_CONNECTED_BLOCKS"
    },
    {
        "LibraryFileName" : "",
        "LibraryParameters" : "",
        "Mode" : "LM_SCAN_DIRECTLY",
        "ScanDirection" : 0,
        "ScanStride" : 0
    },
    {
        "LibraryFileName" : "",
        "LibraryParameters" : "",
        "Mode" : "LM_STATISTICS"
    },
    {
        "LibraryFileName" : "",
        "LibraryParameters" : "",
        "Mode" : "LM_LINES"
    },
    {
        "LibraryFileName" : "",
        "LibraryParameters" : "",
        "Mode" : "LM_STATISTICS_MARKS"
    }
]
```

## Candidate Modes Introduction

### LM_CONNECTED_BLOCKS

Localizes barcodes by searching for connected blocks. This algorithm usually gives best result and it is recommended to set ConnectedBlocks to the highest priority. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- LibraryFileName
- LibraryParameters

### LM_STATISTICS

Localizes barcodes by groups of contiguous black-white regions. This is optimized for QRCode and DataMatrix. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- LibraryFileName
- LibraryParameters

### LM_LINES

Localizes barcodes by searching for groups of lines. This is optimized for 1D and PDF417 barcodes. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- LibraryFileName
- LibraryParameters

### LM_SCAN_DIRECTLY

Localizes barcodes quickly. This mode is recommended in interactive scenario. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- ScanStride
- ScanDirection
- IsOneDStacked
- LibraryFileName
- LibraryParameters

### LM_STATISTICS_MARKS

Localizes barcodes by groups of marks.This is optimized for DPM codes. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- LibraryFileName
- LibraryParameters

### LM_STATISTICS_POSTAL_CODE

Localizes barcodes by groups of connected blocks and lines.This is optimized for postal codes. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- LibraryFileName
- LibraryParameters

### LM_CENTRE

Localizes barcodes from the centre of the image. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- LibraryFileName
- LibraryParameters

### LM_ONED_FAST_SCAN

Localizes 1D barcodes in a fast mode. This mode is designed for reading 1D barcodes in a very fast mode. This mode has the following arguments for further customizing.

**Available auxiliary parameters:**

- ScanStride
- ScanDirection
- ConfidenceThreshold
- LibraryFileName
- LibraryParameters