---
layout: default-layout
Title: ImagePixelFormat - Dynamsoft Core Enumerations
Description: The enumeration ImagePixelFormat of Dynamsoft Core describes all supported image pixel formats.
Keywords: Image pixel format
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImagePixelFormat
---

# Enumeration ImagePixelFormat

`ImagePixelFormat` describes all the supported image pixel formats.

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
    IPF_BGR_888
}ImagePixelFormat;
```
