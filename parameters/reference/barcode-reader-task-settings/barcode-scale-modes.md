---
layout: default-layout
title: BarcodeScaleModes - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeScaleModes of Dynamsoft Barcode Reader defines the scaling mode applied during barcode recognition.
keywords: barcode scale modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BarcodeScaleModes

Parameter `BarcodeScaleModes` defines the scaling mode applied during barcode recognition.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    ├── SectionArray[j]
    │   └── StageArray[k] (Stage object)
    │       └── BarcodeScaleModes
```

**Parent object:** [ScaleBarcodeImageStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-scale-barcode-image.html) object

**Example:**

```json
{
    "BarcodeScaleModes": [
        {
            "Mode": "BSM_AUTO",
            "ModuleSizeThreshold": 0,
            "TargetModuleSize": 0,
            "AcuteAngleWithXThreshold": -1
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `BarcodeScaleModes` parameter.
> - To use it, embed this parameter within a Stage object at the `SST_SCALE_BARCODE_IMAGE` stage.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

Parameter `BarcodeScaleModes` consists of a group of barcode scale mode objects. Each barcode scale mode object includes a candidate mode and a series of auxiliary mode arguments.

### Mode Arguments

The mode arguments of the barcode scale mode object are shown as follows:

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
        <td><b>Candidate Mode List</b><br>BSM_LINEAR_INTERPOLATION
            <br>BSM_AUTO
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">AcuteAngleWithXThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the acute angle threshold for barcode image scale.
        <br>-1: means automatically set by the library.
        <br>The barcode image scaling operation can be performed only if the acute angle between the barcode and the X-axis is greater than the value of AcuteAngleWithXThreshold.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[-1, 90]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>-1
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">ModuleSizeThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the module size threshold for barcode image scale.
        <br>0: means automatically set by the library.
        <br>The scaling logic is as follows:<br>1. If ModuleSizeThreshold < TargetModuleSize, the scale-up logic is applied. If the module size of the barcode is smaller than the ModuleSizeThreshold, the barcode image will be enlarged by a scale factor of N (the value of N is a power of 2) till N * modulesize >= TargetModuleSize.<br>2. If ModuleSizeThreshold > TargetModuleSize, the scale-down logic is applied. If the module size of the barcode is larger than the ModuleSizeThreshold, the barcode image will be shrinked by a scale factor of N (the value of N is a power of 2) till N * modulesize <= TargetModuleSize.<br>If ModuleSizeThreshold = TargetModuleSize, the scaling operation is ignored.
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
        <td rowspan = "4" style="vertical-align:text-top">TargetModuleSize<br>(Optional)</td>
        <td><b>Description</b><br>Sets the module size threshold for barcode image scale.
        <br>0: means automatically set by the library.
        <br>The scaling logic is as follows:<br>1. If ModuleSizeThreshold < TargetModuleSize, the scale-up logic is applied. If the module size of the barcode is smaller than the ModuleSizeThreshold, the barcode image will be enlarged by a scale factor of N (the value of N is a power of 2) till N * modulesize >= TargetModuleSize.<br>2. If ModuleSizeThreshold > TargetModuleSize, the scale-down logic is applied. If the module size of the barcode is larger than the ModuleSizeThreshold, the barcode image will be shrinked by a scale factor of N (the value of N is a power of 2) till N * modulesize <= TargetModuleSize.<br>If ModuleSizeThreshold = TargetModuleSize, the scaling operation is ignored.
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
</table>

### Default Setting

```json
{
    "BarcodeScaleModes": [
        {
            "Mode": "BSM_AUTO",
            "ModuleSizeThreshold": 0,
            "TargetModuleSize": 0,
            "AcuteAngleWithXThreshold": -1
        }
    ]
}
```

## Candidate Mode Introductions

### BSM_AUTO

Lets the library choose a mode automatically. This mode has the following arguments for further customization:

**Available Mode Arguments:**

- AcuteAngleWithXThreshold
- ModuleSizeThreshold
- TargetModuleSize

### BSM_LINEAR_INTERPOLATION

Scales image using the linear interpolation method. This mode has the following arguments for further customization:

**Available Mode Arguments:**

- AcuteAngleWithXThreshold
- ModuleSizeThreshold
- TargetModuleSize

