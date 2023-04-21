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

Parameter `ColourChannelUsageType` specifies how to use the colour channel from the source image buffer.

## Example

```json
{
    "ColourChannelUsageType": "CCUT_NV21_Y_CHANNEL_ONLY"
}
```

## Parameter Summary

| ColourChannelUsageType Parameter Summary |
| :--------------------------------------- |
| **Description**</b><br>There are many ways to represent color images, corresponding to many colour-information channels. |
| **Type**<br>*String* |
| **Range** <br>CCUT_AUTO<br>CCUT_FULL_CHANNEL<br>CCUT_NV21_Y_CHANNEL_ONLY<br>CCUT_RGB_R_CHANNEL_ONLY<br>CCUT_RGB_G_CHANNEL_ONLY<br>CCUT_RGB_B_CHANNEL_ONLY |
| **Default Value**<br>CCUT_AUTO |
