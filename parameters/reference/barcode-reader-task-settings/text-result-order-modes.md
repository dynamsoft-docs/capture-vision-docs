---
layout: default-layout
Title: TextResultOrderModes - Dynamsoft Barcode Reader Parameters
Description: The parameter TextResultOrderModes of Dynamsoft Barcode Reader defines the order of the returned text results.
Keywords: Text result order modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/text-result-order-modes.html
---

# TextResultOrderModes

Parameter `TextResultOrderModes` defines the order of the returned text results.

## Example

```json
{
    "TextResultOrderModes" :
    [
        {
            "Mode" : "TROM_CONFIDENCE"
        },
        {
            "Mode" : "TROM_POSITION"
        },
        {
            "Mode" : "TROM_FORMAT"
        }
    ]
}
```

## Parameter Summary

Parameter `TextResultOrderModes` consist of a group of text result order mode objects. Each text result order mode object includes a candidate mode and a series of auxiliary parameters. The structure of the text result order mode object is shown as follow:

### Child Parameters

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
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
    <tr>
        <td><b>Default Value</b><br>
        </td>
    </tr>
</table>

### Default Setting

If the `TextResultOrderModes` is not configured in your template file, the following setting will be used as the default setting.

```json
{
    "TextResultOrderModes" : 
    [
        {
            "Mode" : "TROM_CONFIDENCE"
        },
        {
            "Mode" : "TROM_POSITION"
        },
        {
            "Mode" : "TROM_FORMAT"
        }
    ]
}
```

## Candidate Modes Introduction

### TROM_CONFIDENCE

Returns the text results in descending order by confidence.

### TROM_POSITION

Returns the text results in position order, from top to bottom, then left to right.

### TROM_FORMAT

Returns the text results in alphabetical and numerical order by barcode format string
