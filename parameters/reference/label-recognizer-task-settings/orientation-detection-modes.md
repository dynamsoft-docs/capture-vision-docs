---
layout: default-layout
title: OrientationDetectionModes - Dynamsoft Label Recognizer Parameters
description: Reference for the OrientationDetectionModes parameter in Dynamsoft Label Recognizer, which enables automatic text line orientation detection using spatial references or neural network models.
keywords: OrientationDetectionModes, parameter reference, parameter
---

# OrientationDetectionModes

Parameter `OrientationDetectionModes` is an array of orientation detection mode objects used in the `SST_LOCALIZE_TEXT_LINES` stage. Each object specifies a method for determining the orientation of detected text lines. Once a mode successfully determines the orientation, subsequent modes in the array are not evaluated. By default, this parameter is `null` and no orientation detection is performed.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.1000.
- **Current limitations** - This capability is currently effective only in MRZ scenarios and supports only upright and upside-down text lines (0 degrees and 180 degrees). It does not yet handle 90 degrees, 270 degrees, or arbitrary rotation angles.

## JSON Structure

**Location in template:**
```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_LOCALIZE_TEXT_LINES")
            └── OrientationDetectionModes
```

**Parent object:** [LocalizeTextLinesStage](stage-localize-text-lines.md)

**Example:**

```json
{
    "OrientationDetectionModes": [
        {
            "Mode": "ODM_SPATIAL_REFERENCES"
        },
        {
            "Mode": "ODM_CHARS_ORIENTATION_NEURAL_NETWORK",
            "ModelNameArray": ["TextLineOrientationCls"]
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `OrientationDetectionModes` parameter.
> - To use it, embed this parameter within a [LocalizeTextLinesStage](stage-localize-text-lines.md) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

Parameter `OrientationDetectionModes` consists of a group of orientation detection mode objects. Each orientation detection mode object includes a candidate mode and a series of mode arguments. The mode arguments of the orientation detection mode object are shown as follows:

### Mode Arguments

<table style="text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan="4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Any one in Candidate Mode List as string
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>ODM_SPATIAL_REFERENCES
            <br>ODM_CHARS_ORIENTATION_NEURAL_NETWORK
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>N/A
        </td>
    </tr>
    <tr>
        <td rowspan="4" style="vertical-align:text-top">ModelNameArray<br>(Optional)</td>
        <td><b>Description</b><br>An array of model names used for neural network-based orientation detection. The default model <code>TextLineOrientationCls</code> supports 0° and 180° orientation detection.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>array of string</i>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>["TextLineOrientationCls"]
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>ODM_CHARS_ORIENTATION_NEURAL_NETWORK
        </td>
    </tr>
</table>

### Candidate Modes

#### ODM_SPATIAL_REFERENCES

Determines text line orientation by analyzing the spatial relationships between reference objects. No additional arguments are available for this mode.

#### ODM_CHARS_ORIENTATION_NEURAL_NETWORK

Determines text line orientation using a neural network model applied to individual text lines. Supports 0° and 180° orientation classification.

**Available Mode Arguments:**

- ModelNameArray