---
layout: default-layout
title: TextureDetectionModes - Dynamsoft Capture Vision Parameters
description: The parameter TextureDetectionModes of Dynamsoft Capture Vision is for detecting texts on an image.
keywords: TextureDetectionModes, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/texture-detection-modes.html
---


# TextureDetectionModes

Parameter TextureDetectionModes controls how to detect texture on an image.

**JSON Parameter Example**   
```json
{
    "TextureDetectionModes": [
        {
            "Mode": "TDM_GENERAL_WIDTH_CONCENTRATION", 
            "Sensitivity": 1
        },
        {
            "Mode": "TDM_GENERAL_WIDTH_CONCENTRATION", 
            "Sensitivity": 9
        }
    ]
}
```

## Parameter Summary
Parameter TextureDetectionModes consists of one or more of the following modes, each mode representing a different preprocessing algorithm:

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
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
        <td><b>Candidate Mode List</b><br>
            <li>TDM_GENERAL_WIDTH_CONCENTRATION</li>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>TDM_GENERAL_WIDTH_CONCENTRATION
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">Sensitivity<br>(Optional)</td>
        <td><b>Description</b><br>Sets the sensitivity used for texture detection. A larger value means the library will take more effort to detect texture.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>	[1, 9]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>5
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
        <li>TDM_GENERAL_WIDTH_CONCENTRATION</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LibraryFileName<br>(Optional)</td>
        <td><b>Description</b><br>Sets the file name of the library to load dynamically.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing file name.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes.
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LibraryParameters<br>(Optional)</td>
        <td><b>Description</b><br>The library must be in the same place with Dynamsoft Barcode Reader Library.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing parameters.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes.
        </td>
    </tr>
</table>

The default settings of TextureDetectionModes is:

```json
{
    "TextureDetectionModes":[
        {
            "Mode": "TDM_GENERAL_WIDTH_CONCENTRATION",
            "Sensitivity": 5
        }
    ]
}
```


## Candidate Modes Introduction

### TDM_GENERAL_WIDTH_CONCENTRATION
Detects texture using the general algorithm. This mode has the following arguments for further customization.

**Available auxiliary parameters:**

- [Sensitivity]()

## See Also
- [Capture Vision Template]()
- [Image Parameter]() 