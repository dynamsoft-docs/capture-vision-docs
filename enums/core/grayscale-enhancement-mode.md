---
layout: default-layout
Title: GrayscaleEnhancementMode - Dynamsoft Core Enumerations
Description: The enumeration GrayscaleEnhancementMode of Dynamsoft Core describes all available grayscale enhancement modes.
Keywords: Grayscale enhancement modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleEnhancementMode
codeAutoHeight: true
---

# Enumeration GrayscaleEnhancementMode

`GrayscaleEnhancementMode` describes the grayscale transformation mode.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
export enum EnumGrayscaleEnhancementMode
{
   /**Not supported yet. */
   GEM_AUTO = 1,
   /**Takes the unpreprocessed image for following operations.*/
   GEM_GENERAL = 2,
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   GEM_GRAY_EQUALIZE = 4,
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   GEM_GRAY_SMOOTH = 8,
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   GEM_SHARPEN_SMOOTH = 16,
   /**Reserved setting for image preprocessing mode.*/
   GEM_REV = -2147483648,
   /**Skips image preprocessing. */
   GEM_SKIP = 0
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumGrayscaleEnhancementMode {
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
