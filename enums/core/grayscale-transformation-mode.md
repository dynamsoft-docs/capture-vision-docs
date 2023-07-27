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
   /** Skips grayscale transformation. */
   GTM_SKIP = 0,
   /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
   GTM_INVERTED = 1,
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   GTM_ORIGINAL = 2,
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   GTM_AUTO = 4,
   /** Reserved setting for grayscale transformation mode. */
   GTM_REV = -2147483648
}
```
>
```java
public class EnumGrayscaleTransformationMode
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
}NS_SWIFT_NAME(GrayscaleTransformationMode);
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
