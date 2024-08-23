---
layout: default-layout
title: QuadrilateralDetectionModes - Dynamsoft Document Normalizer Parameters
description: The parameter QuadrilateralDetectionModes of Dynamsoft Document Normalizer.
keywords: Quadrilateral detection
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# QuadrilateralDetectionModes

Parameter `QuadrilateralDetectionModes` controls the quadrilateral detection process on an image. It currently includes only one mode.

## Example

```json
{
    "QuadrilateralDetectionModes": [
        {
            "Mode": "QDM_GENERAL",
            "MinQuadrilateralAreaRatio" : 30
        }
    ]
}
```

## Parameter Summary

`QuadrilateralDetectionModes` consist one or more mode objects. Each mode object contains a candidate mode and other mode arguments.

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
        <td><b>Description</b><br>Specifies a mode for quadrilateral detection.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br><a href = "#qdm_general">QDM_GENERAL</a><br><a href = "#qdm_skip">QDM_SKIP</a>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>["QDM_GENERAL"]
        </td>
    </tr>
        <tr>
        <td rowspan = "4" style="vertical-align:text-top">MinQuadrilateralAreaRatio<br>(Optional)</td>
        <td><b>Description</b><br>The minimum ratio between the target document area and the total image area. Only those exceeding this value will be outputted (measured in percentages).
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>Int</i>
        </td>
    </tr>
    <tr>
        <td><b>Value Range</b><br>[0,100]</a>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0, indicates the use of automatic exclusion logic to filter out small quads. When this value is changed to anything other than 0, the automatic filtering logic will be disabled.
        </td>
    </tr>
</table>

### Default Setting

If the `QuadrilateralDetectionModes` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "QuadrilateralDetectionModes" : 
    [
        {
            "Mode" : "QDM_GENERAL",
            "MinQuadrilateralAreaRatio" : 0
        }
    ]
}
```

## Candidate Modes Introduction

### QDM_GENERAL

Detects quadrilateral(s) using the general algorithm.

### QDM_SKIP

Skip quadrilateral(s) detection.
