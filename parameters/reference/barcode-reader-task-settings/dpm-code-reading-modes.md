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

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── DPMCodeReadingModes
```

**Parent object:** [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html)

**Example:**

```json
{
    "DPMCodeReadingModes": [
        {
            "Mode": "DPMCRM_GENERAL",
            "BarcodeFormat": "BF_DATAMATRIX"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `DPMCodeReadingModes` parameter.
> - To use it, embed this parameter within a `BarcodeReaderTaskSetting` object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

Parameter `DPMCodeReadingModes` consists of a group of DPM code reading mode objects. Each DPM code reading mode object includes a candidate mode and a series of auxiliary mode arguments.

### Mode Arguments

The mode arguments of the DPM code reading mode object are shown as follows:

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
        <td rowspan = "4" style="vertical-align:text-top">BarcodeFormat<br>(Optional)</td>
        <td><b>Description</b><br>Specifies the format of the DPM barcode to be processed.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>"BF_DATAMATRIX" or "BF_QR_CODE"
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>"BF_DATAMATRIX"
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

If the `DPMCodeReadingModes` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "DPMCodeReadingModes": [
        {
            "Mode" : "DPMCRM_SKIP"
        }
    ]
}
```

## Candidate Mode Introductions

### DPMCRM_GENERAL

Reads DPM codes using the general algorithm. This mode has the following arguments for further customizing.

- BarcodeFormat
- LibraryFileName
- LibraryParameters

### DPMCRM_AUTO

Lets the library choose a mode automatically. Not supported yet.
