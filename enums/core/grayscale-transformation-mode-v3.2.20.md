---
layout: default-layout
title: GrayscaleTransformationMode - Dynamsoft Core Enumerations
description: The enumeration GrayscaleTransformationMode of Dynamsoft Core describes all available grayscale transformation modes.
keywords: Grayscale transformation modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleTransformationMode
codeAutoHeight: true
---

# Enumeration GrayscaleTransformationMode

`GrayscaleTransformationMode` specifies the method employed to transform images in grayscale.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumGrayscaleTransformationMode
{
    /**
     * Bypasses grayscale transformation, leaving the image in its current state without any modification to its grayscale values.
     * This mode is selected when no alteration of the grayscale data is desired, passing the image through to subsequent operations without modification.
     */
    GTM_SKIP = 0,
    /**
     * Applies an inversion to the grayscale values of the image, effectively transforming light elements to dark and vice versa.
     * This mode is particularly useful for images with light text on dark backgrounds, enhancing visibility for further processing.
     */
    GTM_INVERTED = 1,
    /**
     * Maintains the original grayscale values of the image without any transformation. This mode is suited for images with
     * dark elements on light backgrounds, ensuring the natural contrast and detail are preserved for subsequent analysis.
     */
    GTM_ORIGINAL = 2,
    /**
     * Delegates the choice of grayscale transformation to the library's algorithm, which automatically determines the most
     * suitable transformation based on the image's characteristics. This mode is beneficial when the optimal transformation
     * is not known in advance or varies across different images.
     */
    GTM_AUTO = 4,
    /**
     * Reserved for future expansion or internal use. This placeholder indicates a grayscale transformation mode that is
     * not currently defined for public use but may be utilized for upcoming features or reserved for specific, undocumented adjustments.
     */
    GTM_REV = -2147483648
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumGrayscaleTransformationMode
{
   /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
   public static final int GTM_INVERTED = 1;
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   public static final int GTM_ORIGINAL = 2;
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   public static final int GTM_AUTO = 4;
   /** Skips grayscale transformation. */
   public static final int GTM_SKIP = 0;
   /** Reserved setting for grayscale transformation mode. */
   public static final int GTM_REV = -2147483648;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSGrayscaleTransformationMode)
{
   /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
   DSGrayscaleTransformationModeInverted = 0x01,
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   DSGrayscaleTransformationModeOriginal = 0x02,
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   DSGrayscaleTransformationModeAuto     = 0x04,
   /** Skips grayscale transformation. */
   DSGrayscaleTransformationModeSkip     = 0x00,
   /** Reserved setting for grayscale transformation mode. */
   DSGrayscaleTransformationModeRev      = -2147483648
};
```
>
```swift
public enum GrayscaleTransformationMode : Int
{
   /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
   inverted = 0x01
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   original = 0x02
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   auto     = 0x04
   /** Skips grayscale transformation. */
   skip     = 0x00
   /** Reserved setting for grayscale transformation mode. */
   rev      = -2147483648
}
```
>
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
