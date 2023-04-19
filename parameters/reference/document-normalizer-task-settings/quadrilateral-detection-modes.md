---
layout: default-layout
Title: QuadrilateralDetectionModes - Dynamsoft Document Normalizer Parameters
Description: The parameter QuadrilateralDetectionModes of Dynamsoft Document Normalizer is XXX.
Keywords: Quadrilateral detection
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/document-normalizer-task-settings/quadrilateral-detection-modes.html
---

# QuadrilateralDetectionModes

`QuadrilateralDetectionModes` controls the quadrilateral detection process on an image. It currently includes only one mode.

```json
{
    "QuadrilateralDetectionModes": [
        {
            "Mode": "QDM_GENERAL"
        }
    ]
}
```

`QuadrilateralDetectionModes` consist one or more mode objects. Each mode object contains a candidate mode and other auxiliary parameters.

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
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
        <td><b>Candidate Mode List</b><br><br><a href = "#dmperspectivecorrection">QDM_GENERAL</a>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>["QDM_GENERAL"]
        </td>
    </tr>
</table>

## Modes Paraphrase

### QDM_GENERAL

Detects quadrilateral(s) using the general algorithm.
