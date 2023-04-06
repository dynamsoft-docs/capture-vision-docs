---
layout: default-layout
Title: InteriorAngleRangeArray - Dynamsoft Document Normalizer Parameters
Description: The parameter InteriorAngleRangeArray of Dynamsoft Document Normalizer is XXX.
Keywords:
needAutoGenerateSidebar: true
noTitleIndex: true
---

# InteriorAngleRangeArray

`InteriorAngleRangeArray` specifies the range of angles (in degrees) of the extracted corners. The corners refer to the corners of the quad or document.

```json
{
    "InteriorAngleRangeArray":
    [
        {
            "MinValue": 70,
            "MaxValue": 110
        }
    ]
}
```

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Details</th>
    </tr>
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
        <td><b>Range</b><br>[0,180]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>70
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
        <td><b>Range</b><br>[0,180]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>110</td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>The sum of MinValue and MaxValue should be 180. If the values you input doesn't meet the requirement, they will be adjusted by the library automatically.
        </td>
    </tr>
</table>