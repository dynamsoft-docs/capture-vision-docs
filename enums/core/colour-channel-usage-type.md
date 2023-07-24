---
layout: default-layout
Title: ColourChannelUsageType - Dynamsoft Core Enumerations
Description: The enumeration ColourChannelUsageType of Dynamsoft Core describes how the color channel is used in the image.
Keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ColourChannelUsageType
---

# Enumeration ColourChannelUsageType

`ColourChannelUsageType` describes how the color channel is used in the image.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
export enum EnumColourChannelUsageType
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
    CCUT_AUTO = 0,
    /** Use all available color channels for processing. */
    CCUT_FULL_CHANNEL = 1,
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
    CCUT_NV21_Y_CHANNEL_ONLY = 2,
    /** Use only the red channel for processing in RGB images.*/
    CCUT_RGB_R_CHANNEL_ONLY = 3,
    /** Use only the green channel for processing in RGB images.*/
    CCUT_RGB_G_CHANNEL_ONLY = 4,
    /** Use only the blue channel for processing in RGB images.*/
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
