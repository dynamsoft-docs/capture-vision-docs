---
layout: default-layout
title: IfEraseTextZone - Dynamsoft Capture Vision Parameters
description: The parameter IfEraseTextZone of Dynamsoft Capture Vision is for controlling whether to erase the detected text zone.
keywords: IfEraseTextZone, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/image-parameter/if-erase-text-zone.html
---


# IfEraseTextZone

Parameter IfEraseTextZone sets whether to erase the detected text zone. The detected text zone is the result of text detection process when enables TextDetectionMode.
>- Do not erase text when a text recognition task is to be performed.

## Example

```json
{
    "IfEraseTextZone": 1
}
```

## Parameter Summary

### Child Parameters

Parameter IfEraseTextZone determines whether to erase text:

<table style = "text-align:left">
    <tr>
        <th>IfEraseTextZone Parameter Details</th>
    </tr>
    <tr>
        <td><b>Description</b><br>0: Do not erase the text zone.<br>1: Erase the text zone.</li>
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Value range</b><br>[0,1]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
</table>

### Default Setting

The default settings of IfEraseTextZone is:

```json
{
    "IfEraseTextZone": 0
}
```

## See Also
- [Capture Vision Template]()
- [Image Parameter]() 