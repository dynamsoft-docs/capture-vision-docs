---
layout: default-layout
title: CornerAngleRange - Dynamsoft Document Normalizer Parameters
description: The parameter CornerAngleRange specifies the range of angles of the extracted corners.
keywords: CornerAngleRange
---

# CornerAngleRange

`CornerAngleRange` specifies the range of angles (in degrees) of the extracted corners. The corners refer to the corners of a quad or document.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_DETECT_CORNERS")
            └── CornerAngleRange
```

**Parent object:** [DetectCornersStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-detect-corners.html)

**Example:**

```json
{
    "CornerAngleRange": {
        "MinValue": 80,
        "MaxValue": 100
    }
}
```

> [!NOTE]
> - This snippet shows only the `CornerAngleRange` parameter.
> - To use it, embed this parameter within a [DetectCornersStage]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/stage-detect-corners.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

`CornerAngleRange` The range of a maximum and a minimum value of the angles.

### Child Parameters

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">MinValue</td>
        <td><b>Description</b><br>Sets the minimum interior angle.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,90]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>60
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">MaxValue</td>
        <td><b>Description</b><br>Sets the maximum interior angle.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[90,180]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>120</td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>Please ensure that all interior angles of the target quadrilateral fall within the specified value range.
        <br>If the setting values doesn't meet the requirement ranges, an error will be raised.
        </td>
    </tr>
</table>

### Default Setting

If the `CornerAngleRange` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "CornerAngleRange" : 
        {
            "MaxValue" : 120,
            "MinValue" : 60
        }
}
```
