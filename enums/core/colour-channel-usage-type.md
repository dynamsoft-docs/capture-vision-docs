---
layout: default-layout
title: ColourChannelUsageType - Dynamsoft Core Enumerations
description: The enumeration ColourChannelUsageType of Dynamsoft Core describes how the color channel is used in the image.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ColourChannelUsageType
codeAutoHeight: true
---

# Enumeration ColourChannelUsageType

`ColourChannelUsageType` enumerates the different ways color channels can be utilized in image processing. This allows for flexible image analysis and manipulation by specifying how color data should be handled.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >- C#
   >- Python
   >
>
```javascript
enum EnumColourChannelUsageType {
    /**
     * Automatically determines how color channels are used.
     * This option allows the SDK to choose the most appropriate channel usage mode dynamically.
     */
    CCUT_AUTO = 0,
    /**
     * Utilizes all available color channels in the image for processing.
     * This mode is ideal for scenarios where full color information is necessary for accurate analysis or processing.
     */
    CCUT_FULL_CHANNEL = 1,
    /**
     * Processes images using only the Y (luminance) channel, specifically in NV21 format images.
     * This mode is useful for operations that require analyzing the brightness or intensity of the image while ignoring color information.
     */
    CCUT_Y_CHANNEL_ONLY = 2,
    /**
     * Uses only the red color channel for processing in RGB images.
     * This mode is useful for tasks that require analysis or manipulation based on the red component of the image.
     */
    CCUT_RGB_R_CHANNEL_ONLY = 3,
    /**
     * Uses only the green color channel for processing in RGB images.
     * This mode is useful for tasks where the green component is most relevant.
     */
    CCUT_RGB_G_CHANNEL_ONLY = 4,
    /**
     * Uses only the blue color channel for processing in RGB images.
     * This mode is useful for tasks where the blue component is of particular interest.
     */
    CCUT_RGB_B_CHANNEL_ONLY = 5
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumColourChannelUsageType
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
    public static final int CCUT_AUTO = 0;
    /** Use all available color channels for processing. */
    public static final int CCUT_FULL_CHANNEL = 1;
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
    public static final int CCUT_NV21_Y_CHANNEL_ONLY = 2;
    /** Use only the red channel for processing in RGB images.*/
    public static final int CCUT_RGB_R_CHANNEL_ONLY = 3;
    /** Use only the green channel for processing in RGB images.*/
    public static final int CCUT_RGB_G_CHANNEL_ONLY = 4;
    /** Use only the blue channel for processing in RGB images.*/
    public static final int CCUT_RGB_B_CHANNEL_ONLY = 5;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSColourChannelUsageType)
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
    DSColourChannelUsageTypeAuto = 0,
    /** Use all available color channels for processing. */
    DSColourChannelUsageTypeFullChannel = 1,
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
    DSColourChannelUsageTypeNV21YChannelOnly = 2,
    /** Use only the red channel for processing in RGB images.*/
    DSColourChannelUsageTypeRGBRChannelOnly = 3,
    /** Use only the green channel for processing in RGB images.*/
    DSColourChannelUsageTypeRGBGChannelOnly = 4,
    /** Use only the blue channel for processing in RGB images.*/
    DSColourChannelUsageTypeRGBBChannelOnly = 5
};
```
>
```swift
public enum ColourChannelUsageType : Int
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
   auto = 0,
    /** Use all available color channels for processing. */
   fullChannel = 1,
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
   nv21YChannelOnly = 2,
    /** Use only the red channel for processing in RGB images.*/
   rgbrChannelOnly = 3,
    /** Use only the green channel for processing in RGB images.*/
   rgbgChannelOnly = 4,
    /** Use only the blue channel for processing in RGB images.*/
   rgbbChannelOnly = 5
};
```
>
```cpp
typedef enum ColourChannelUsageType
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
    CCUT_AUTO,
    /** Use all available color channels for processing. */
    CCUT_FULL_CHANNEL,
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
    CCUT_NV21_Y_CHANNEL_ONLY,
    /** Use only the red channel for processing in RGB images.*/
    CCUT_RGB_R_CHANNEL_ONLY,
    /** Use only the green channel for processing in RGB images.*/
    CCUT_RGB_G_CHANNEL_ONLY,
    /** Use only the blue channel for processing in RGB images.*/
    CCUT_RGB_B_CHANNEL_ONLY
} ColourChannelUsageType;
```
>
```csharp
public enum EnumColourChannelUsageType
{
    /**Automatic color channel usage determination based on image pixel format and scene.*/
    CCUT_AUTO,
    /**Use all available color channels for processing.*/
    CCUT_FULL_CHANNEL,
    /**Use only the Y(luminance) channel for processing in images represented in the NV21 format.*/
    CCUT_Y_CHANNEL_ONLY,
    /**Use only the red channel for processing in RGB images.*/
    CCUT_RGB_R_CHANNEL_ONLY,
    /**Use only the green channel for processing in RGB images.*/
    CCUT_RGB_G_CHANNEL_ONLY,
    /**Use only the blue channel for processing in RGB images.*/
    CCUT_RGB_B_CHANNEL_ONLY
}
```
>
```python
class EnumColourChannelUsageType(IntEnum):
    #Automatic color channel usage determination based on image pixel format and scene.
    CCUT_AUTO
    #Use all available color channels for processing.
    CCUT_FULL_CHANNEL
    #Use only the Y(luminance) channel for processing in images represented in the NV21 format.
    CCUT_Y_CHANNEL_ONLY
    #Use only the red channel for processing in RGB images.
    CCUT_RGB_R_CHANNEL_ONLY
    #Use only the green channel for processing in RGB images.
    CCUT_RGB_G_CHANNEL_ONLY
    #Use only the blue channel for processing in RGB images.
    CCUT_RGB_B_CHANNEL_ONLY
```
