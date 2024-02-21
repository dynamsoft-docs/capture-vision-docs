---
layout: default-layout
title: ImagePixelFormat - Dynamsoft Core Enumerations
description: The enumeration ImagePixelFormat of Dynamsoft Core describes all supported image pixel formats.
keywords: Image pixel format
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImagePixelFormat
codeAutoHeight: true
---

# Enumeration ImagePixelFormat

`ImagePixelFormat` defines the range of pixel formats that an image can have, specifying how color and transparency data are represented in each pixel of the image.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumImagePixelFormat {
   /** Binary format representing images with two colors: 0 for black and 1 for white. */
   IPF_BINARY = 0,
   /** Inverted binary format with 0 for white and 1 for black. */
   IPF_BINARYINVERTED = 1,
   /** Grayscale format with 8 bits per pixel, allowing for 256 shades of gray. */
   IPF_GRAYSCALED = 2,
   /** NV21 format, a YUV planar format used commonly in camera preview and video encoding, with 8-bit Y followed by interleaved V/U values. */
   IPF_NV21 = 3,
   /** RGB format with 5 bits for red and blue, and 6 bits for green, stored in a 16-bit structure. */
   IPF_RGB_565 = 4,
   /** Similar to RGB_565 but with 5 bits for each color channel, providing uniform color depth across channels in a 16-bit structure. */
   IPF_RGB_555 = 5,
   /** Standard 24-bit RGB format with 8 bits per channel. */
   IPF_RGB_888 = 6,
   /** 32-bit ARGB format with 8 bits per channel, including an alpha channel for transparency. */
   IPF_ARGB_8888 = 7,
   /** High-depth 48-bit RGB format with 16 bits per channel. */
   IPF_RGB_161616 = 8,
   /** 64-bit ARGB format with 16 bits per channel, including an alpha channel. */
   IPF_ARGB_16161616 = 9,
   /** 32-bit ABGR format with 8 bits per channel, storing color information in reverse order of ARGB_8888. */
   IPF_ABGR_8888 = 10,
   /** 64-bit ABGR format with 16 bits per channel, providing high color depth and transparency in the reverse order of ARGB_16161616. */
   IPF_ABGR_16161616 = 11,
   /** 24-bit BGR format with 8 bits per channel, where the blue channel is stored first. */
   IPF_BGR_888 = 12,
   /** Binary format with 8 bits per pixel, enabling more detailed binary images by allowing for antialiasing or other binary representations. */
   IPF_BINARY_8 = 13,
   /** NV12 format, similar to NV21 but with the U and V color components swapped. */
   IPF_NV12 = 14
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumCapturedResultItemType
{
   /** 0:Black, 1:White. */
   public static final int IPF_BINARY = 0;
   /** 0:White, 1:Black. */
   public static final int IPF_BINARYINVERTED = 1;
   /** 8bit gray. */
   public static final int IPF_GRAYSCALED = 2;
   /** NV21. */
   public static final int IPF_NV21 = 3;
   /** 16bit with RGB channel order stored in memory from high to low address. */
   public static final int IPF_RGB_565 = 4;
   /** 16bit with RGB channel order stored in memory from high to low address. */
   public static final int IPF_RGB_555 = 5;
   /** 24bit with RGB channel order stored in memory from high to low address. */
   public static final int IPF_RGB_888 = 6;
   /** 32bit with ARGB channel order stored in memory from high to low address. */
   public static final int IPF_ARGB_8888 = 7;
   /** 48bit with RGB channel order stored in memory from high to low address. */
   public static final int IPF_RGB_161616 = 8;
   /** 64bit with ARGB channel order stored in memory from high to low address. */
   public static final int IPF_ARGB_16161616 = 9;
   /** 32bit with ABGR channel order stored in memory from high to low address. */
   public static final int IPF_ABGR_8888 = 10;
   /** 64bit with ABGR channel order stored in memory from high to low address. */
   public static final int IPF_ABGR_16161616 = 11;
   /** 24bit with BGR channel order stored in memory from high to low address. */
   public static final int IPF_BGR_888 = 12;
   /** 0:Black, 255:White. */
   public static final int IPF_BINARY_8 = 13;
   /**NV12 */
   public static final int IPF_NV12 = 14;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSImagePixelFormat)
{
   /** 0:black, 1:white */
   DSImagePixelFormatBinary,
   /** 0:white, 1:black */
   DSImagePixelFormatBinaryInverted,
   /** 8-bit gray */
   DSImagePixelFormatGrayScaled,
   /** NV21 */
   DSImagePixelFormatNV21,
   /** 16bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB_565,
   /** 16bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB_555,
   /** 24bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB_888,
   /** 32bit with ARGB channel order stored in memory from high to low address*/
   DSImagePixelFormatARGB_8888,
   /** 48bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB_161616,
   /** 64bit with ARGB channel order stored in memory from high to low address*/
   DSImagePixelFormatARGB_16161616,
   /** 32bit with ABGB channel order stored in memory from high to low address */
   DSImagePixelFormatABGR_8888,
   /** 64bit with ABGR channel order stored in memory from high to low address*/
   DSImagePixelFormatABGR_16161616,
   /** 24bit with BGR channel order stored in memory from high to low address*/
   DSImagePixelFormatBGR_888,
   /**  0:black, 255:white */
   DSImagePixelFormatBinary_8,
   /**NV12 */
   DSImagePixelFormatNV12
};
```
>
```swift
public enum ImagePixelFormat : Int
{
   /** 0:black, 1:white */
   binary
   /** 0:white, 1:black */
   binaryInverted
   /** 8-bit gray */
   grayScaled
   /** NV21 */
   NV21
   /** 16bit with RGB channel order stored in memory from high to low address*/
   RGB_565
   /** 16bit with RGB channel order stored in memory from high to low address*/
   RGB_555
   /** 24bit with RGB channel order stored in memory from high to low address*/
   RGB_888
   /** 32bit with ARGB channel order stored in memory from high to low address*/
   ARGB_8888
   /** 48bit with RGB channel order stored in memory from high to low address*/
   RGB_161616
   /** 64bit with ARGB channel order stored in memory from high to low address*/
   ARGB_16161616
   /** 32bit with ABGB channel order stored in memory from high to low address */
   ABGR_8888
   /** 64bit with ABGR channel order stored in memory from high to low address*/
   ABGR_16161616
   /** 24bit with BGR channel order stored in memory from high to low address*/
   BGR_888
   /**  0:black, 255:white */
   binary_8
   /**NV12 */
   NV12
}
```
>
```cpp
typedef enum ImagePixelFormat
{
   /** 0:Black, 1:White. */
   IPF_BINARY,
   /** 0:White, 1:Black. */
   IPF_BINARYINVERTED,
   /** 8bit gray. */
   IPF_GRAYSCALED,
   /** NV21. */
   IPF_NV21,
   /** 16bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_565,
   /** 16bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_555,
   /** 24bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_888,
   /** 32bit with ARGB channel order stored in memory from high to low address. */
   IPF_ARGB_8888,
   /** 48bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_161616,
   /** 64bit with ARGB channel order stored in memory from high to low address. */
   IPF_ARGB_16161616,
   /** 32bit with ABGR channel order stored in memory from high to low address. */
   IPF_ABGR_8888,
   /** 64bit with ABGR channel order stored in memory from high to low address. */
   IPF_ABGR_16161616,
   /** 24bit with BGR channel order stored in memory from high to low address. */
   IPF_BGR_888,
   /** 0:Black, 255:White. */
   IPF_BINARY_8,
   /**NV12 */
   IPF_NV12
}ImagePixelFormat;
```
