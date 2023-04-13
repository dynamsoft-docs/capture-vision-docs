---
layout: default-layout
Title: GrayscaleTransformationMode - Dynamsoft Core Enumerations
Description: The enumeration GrayscaleTransformationMode of Dynamsoft Core describes all available grayscale transformation modes.
Keywords: Grayscale transformation modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleTransformationMode
---

# Enumeration GrayscaleTransformationMode

`GrayscaleTransformationMode` describes the grayscale transformation mode.

```cpp
typedef enum GrayscaleTransformationMode
{
    /** Transforms to inverted grayscale. Recommended for light on dark images. */
    GTM_INVERTED = 0x01,
    /** Keeps the original grayscale. Recommended for dark on light images. */
    GTM_ORIGINAL = 0x02,
    /** Lets the library choose an algorithm automatically for grayscale transformation. */
    GTM_AUTO = 0x04,
    /** Reserved setting for grayscale transformation mode. */
#if defined(_WIN32) || defined(_WIN64)
    GTM_REV = 0x80000000,
#else
    GTM_REV = -2147483648,
#endif
    /** Skips grayscale transformation. */
    GTM_SKIP = 0x00
}GrayscaleTransformationMode;
```
