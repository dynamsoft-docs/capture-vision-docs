---
layout: default-layout
Title: LineExtractionModes - Dynamsoft Document Normalizer Parameters
Description: The parameter LineExtractionModes of Dynamsoft Document Normalizer is XXX.
Keywords:
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LineExtractionModes

`LineExtractionModes` specifies the algorithm used to extract lines. It currently consist of `LEM_GENERAL` and `LEM_MARGIN_BASED`. Each mode representing a different way to extract lines.

```json
{
    "LineExtractionModes":
    [
        {
            "Mode": "LEM_GENERAL"
        },
        {
            "Mode": "LEM_MARGIN_BASED" 
        }
    ]
}
```

`LineExtractionModes` consist one or more mode objects. Each mode object contains a candidate mode and other auxiliary parameters.

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Specifies a mode for line extraction.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>
            <li><a href = "#lemgeneral">LEM_GENERAL</a>
            <li><a href = "#lemmarginbased">LEM_MARGIN_BASED</a>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>["LEM_GENERAL"]
        </td>
    </tr>
</table>

## Candidate Modes Paraphrase

### LEM_GENERAL

Designed for the senarios where the document background colour is distinct from the environment background colour. In these scenarios, contours of the document bounaries are clear enough on the binary images. As a result, the line segments can be easily extracted from the image.

### LEM_MARGIN_BASED

Designed for the senarios where the background colour is similar to the environment background colour. For these scenarios, it is hard to get distinct contours of document boundaries with general binarization process. When the mode `LEM_MARGIN_BASED` is enabled, the library will implement different parameters for the binarization mode to separate the document contents and the background areas. The line segments of the document boundaries will be extracted from the margin between document contents and the background areas.
