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

`ImagePixelFormat` describes all the supported image pixel formats.

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
   /** 0:Black, 1:White. */
   IPF_BINARY = 0,
   /** 0:White, 1:Black. */
   IPF_BINARYINVERTED = 1,
   /** 8bit gray. */
   IPF_GRAYSCALED = 2,
   /** NV21. */
   IPF_NV21 = 3,
   /** 16bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_565 = 4,
   /** 16bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_555 = 5,
   /** 24bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_888 = 6,
   /** 32bit with ARGB channel order stored in memory from high to low address. */
   IPF_ARGB_8888 = 7,
   /** 48bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_161616 = 8,
   /** 64bit with ARGB channel order stored in memory from high to low address. */
   IPF_ARGB_16161616 = 9,
   /** 32bit with ABGR channel order stored in memory from high to low address. */
   IPF_ABGR_8888 = 10,
   /** 64bit with ABGR channel order stored in memory from high to low address. */
   IPF_ABGR_16161616 = 11,
   /** 24bit with BGR channel order stored in memory from high to low address. */
   IPF_BGR_888 = 12,
   /** 0:Black, 255:White. */
   IPF_BINARY_8 = 13,
   /**NV12 */
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
