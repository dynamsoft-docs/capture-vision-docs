---
layout: default-layout
title: GrayscaleEnhancementMode - Dynamsoft Core Enumerations
description: The enumeration GrayscaleEnhancementMode of Dynamsoft Core describes all available grayscale enhancement modes.
keywords: Grayscale enhancement modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleEnhancementMode
codeAutoHeight: true
---

# Enumeration GrayscaleEnhancementMode

`GrayscaleEnhancementMode` specifies the method employed to enhance images in grayscale.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumGrayscaleEnhancementMode
{
    /**
     * Disables any grayscale image preprocessing. Selecting this mode skips the preprocessing step,
     * passing the image through to subsequent operations without modification.
     */
    GEM_SKIP = 0,
    /**
     * Automatic selection of grayscale enhancement mode. Currently, not supported.
     * Future implementations may automatically choose the most suitable enhancement based on image analysis.
     */
    GEM_AUTO = 1,
    /**
     * Uses the original, unprocessed image for subsequent operations. This mode is selected when no specific
     * grayscale enhancement is required, maintaining the image in its natural state.
     */
    GEM_GENERAL = 2,
    /**
     * Applies a grayscale equalization algorithm to the image, enhancing contrast and detail in gray level.
     * Suitable for images with poor contrast.
     */
    GEM_GRAY_EQUALIZE = 4,
    /**
     * Implements a grayscale smoothing algorithm to reduce noise and smooth the image.
     * This can be beneficial for images with high levels of grain or noise.
     */
    GEM_GRAY_SMOOTH = 8,
    /**
     * Enhances the image by applying both sharpening and smoothing algorithms. This mode aims to increase
     * clarity and detail while reducing noise, offering a balanced approach to image preprocessing.
     */
    GEM_SHARPEN_SMOOTH = 16,
    /**
     * Reserved for future use. This setting is part of the grayscale enhancement mode but is
     * currently not defined for public use. It's reserved for internal development or future enhancements. 
     */
    GEM_REV = -2147483648
}
```
>
```java
@Retention(RetentionPolicy.CLASS)public @interface EnumGrayscaleEnhancementMode {
   /**Not supported yet. */
   public static final int GEM_AUTO = 1;
   /**Takes the unpreprocessed image for following operations.*/
   public static final int GEM_GENERAL = 2;
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   public static final int GEM_GRAY_EQUALIZE = 4;
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   public static final int GEM_GRAY_SMOOTH = 8;
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   public static final int GEM_SHARPEN_SMOOTH = 16;
   /**Reserved setting for image preprocessing mode.*/
   public static final int GEM_REV = -2147483648;
   /**Skips image preprocessing. */
   public static final int GEM_SKIP = 0;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSGrayscaleEnhancementMode)
{
   /**Not supported yet. */
   DSGrayscaleEnhancementModeAuto = 1,
   /**Takes the unpreprocessed image for following operations.*/
   DSGrayscaleEnhancementModeGeneral = 2,
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   DSGrayscaleEnhancementModeGrayEqualize = 4,
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   DSGrayscaleEnhancementModeGraySmooth = 8,
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   DSGrayscaleEnhancementModeSharpenSmooth = 16,
   /**Reserved setting for image preprocessing mode.*/
   DSGrayscaleEnhancementModeRev = -2147483648,
   /**Skips image preprocessing. */
   DSGrayscaleEnhancementModeSkip = 0
};
```
>
```swift
public enum GrayscaleEnhancementMode : Int
{
   /**Not supported yet. */
   auto = 1
   /**Takes the unpreprocessed image for following operations.*/
   general = 2
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   grayEqualize = 4
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   graySmooth = 8
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   sharpenSmooth = 16
   /**Reserved setting for image preprocessing mode.*/
   rev = -2147483648
   /**Skips image preprocessing. */
   skip = 0
}
```
>
```cpp
typedef enum GrayscaleEnhancementMode
{
   /**Not supported yet. */
   GEM_AUTO = 0x01,
   /**Takes the unpreprocessed image for following operations. */
   GEM_GENERAL = 0x02,
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   GEM_GRAY_EQUALIZE = 0x04,
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   GEM_GRAY_SMOOTH = 0x08,
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   GEM_SHARPEN_SMOOTH = 0x10,
   /**Reserved setting for image preprocessing mode.*/
#if defined(_WIN32) || defined(_WIN64)
   GEM_REV = 0x80000000,
#else
   GEM_REV = -2147483648,
#endif
   /**Skips image preprocessing. */
   GEM_SKIP = 0x00
}GrayscaleEnhancementMode;
```
