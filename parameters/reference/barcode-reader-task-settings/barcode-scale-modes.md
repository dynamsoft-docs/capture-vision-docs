---
layout: default-layout
title: BarcodeScaleModes - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeScaleModes of Dynamsoft Barcode Reader defines scaling mode applied during barcode recognition.
keywords: barcode scale
---

# BarcodeScaleModes

Parameter `BarcodeScaleModes` defines the scaling mode applied during barcode recognition.

## Example

```json
{
    "BarcodeScaleModes": 
    [
        {
            "Mode": "BSM_LINEAR_INTERPOLATION", 
            "ModuleSizeThreshold": 4,
            "TargetModuleSize": 8,
            "AcuteAngleWithXThreshold": -1
        },
    ]
}
```

## Parameter Summary

Parameter `BarcodeScaleModes` consist of a group of scale mode objects. Each scale mode object includes a candidate mode and a series of mode arguments. The mode arguments of the scale mode object is shown as follow:

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
        <td><b>Candidate Mode List</b><br>BSM_LINEAR_INTERPOLATION
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        <br>BSM_LINEAR_INTERPOLATION
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

If the `BarcodeScaleModes` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "BarcodeScaleModes" : 
    [
        {
            "Mode" : "BSM_LINEAR_INTERPOLATION",
            "ModuleSizeThreshold" : 0,
            "TargetModuleSize" : 0,
            "AcuteAngleWithXThreshold" : -1
        }
    ]
}
```

## Candidate Modes Introduction

### BSM_LINEAR_INTERPOLATION

Scales image using the linear interpolation method. This mode has the following arguments for further customizing:

- AcuteAngleWithXThreshold
- ModuleSizeThreshold
- TargetModuleSize

