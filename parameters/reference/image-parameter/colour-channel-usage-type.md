---
layout: default-layoutColourChannelUsageType
title: ColourChannelUsageType - Dynamsoft Capture Vision Parameters
description: The parameter ColourChannelUsageType of Dynamsoft Capture Vision is for specifing how to use the colour channel from the source image buffer.
keywords: ColourChannelUsageType, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /parameters/reference/image-parameter/colour-channel-usage-type.html
---


# ColourChannelUsageType

ColourChannelUsageType specifies how to use the colour channel from the source image buffer.

## Example

```json
{
    "ColourChannelUsageType": "CCUT_NV21_Y_CHANNEL_ONLY"
}
```

## Parameter Summary

Parameter ColourChannelUsageType allows to use only the information of the specified color channel when loading the image:

### Child Parameters

<table style = "text-align:left">
    <tr>
        <th>ColourChannelUsageType Parameter Details</th>
    </tr>
    <tr>
        <td><b>Description</b><br>
        There are many ways to represent color images, corresponding to many colour-information channels.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>string</i>
        </td>
    </tr>
    <tr>
        <td><b>Value range</b>
        <li>"CCUT_AUTO"</li>
        <li>"CCUT_FULL_CHANNEL"</li>
        <li>"CCUT_NV21_Y_CHANNEL_ONLY"</li>
        <li>"CCUT_RGB_R_CHANNEL_ONLY"</li>
        <li>"CCUT_RGB_G_CHANNEL_ONLY"</li>
        <li>"CCUT_RGB_B_CHANNEL_ONLY"</li>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>“CCUT_AUTO”
        </td>
    </tr>
    
</table>

### Default Setting

The default settings of ColourChannelUsageType is:

```json
{
    "ColourChannelUsageType": "CCUT_AUTO"
}
```

## See Also
- [Capture Vision Template]()
- [Image Parameter]() 