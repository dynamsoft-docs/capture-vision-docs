---
layout: default-layout
title: TextResultOrderModes - Dynamsoft Barcode Reader Parameters
description: The parameter TextResultOrderModes of Dynamsoft Barcode Reader defines the order of the returned text results.
keywords: Text result order modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextResultOrderModes

Parameter `TextResultOrderModes` defines the order of the returned text results. It consists of one or more modes, each mode representing a different ordering criterion.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── TextResultOrderModes
```

**Parent object:** [BarcodeReaderTaskSetting]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/index.html) object

**Example:**

```json
{
    "TextResultOrderModes": [
        {
            "Mode": "TROM_CONFIDENCE"
        },
        {
            "Mode": "TROM_POSITION"
        },
        {
            "Mode": "TROM_FORMAT"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `TextResultOrderModes` parameter.
> - To use it, embed this parameter within a [BarcodeReaderTaskSetting]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/index.html) object at the task-level.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

Parameter `TextResultOrderModes` consists of a group of text result order mode objects. Each text result order mode object includes a candidate mode and a series of auxiliary mode arguments.

### Mode Arguments

The mode arguments of the text result order mode object are as follows:

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
        <td><b>Description</b><br>Specifies a mode for ordering.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>TROM_CONFIDENCE
            <br>TROM_POSITION
            <br>TROM_FORMAT
            <br>TROM_SKIP
        </td>
    </tr>
</table>

### Default Setting

If the `TextResultOrderModes` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "TextResultOrderModes": [
        {
            "Mode": "TROM_CONFIDENCE"
        },
        {
            "Mode": "TROM_POSITION"
        },
        {
            "Mode": "TROM_FORMAT"
        }
    ]
}
```

## Candidate Mode Introductions

### TROM_CONFIDENCE

Returns the text results in descending order by confidence.

### TROM_POSITION

Returns the text results in position order, from top to bottom, then left to right.

### TROM_FORMAT

Returns the text results in alphabetical and numerical order by barcode format string
