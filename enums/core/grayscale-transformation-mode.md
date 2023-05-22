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
export enum EnumGrayscaleTransformationMode
{
   GTM_SKIP = 0,
   GTM_INVERTED = 1,
   GTM_ORIGINAL = 2,
   GTM_AUTO = 4,
   GTM_REV = -2147483648
}
```
>
```java
public class EnumGrayscaleTransformationMode
{
   public static final int GTM_INVERTED = 1;
   public static final int GTM_ORIGINAL = 2;
   public static final int GTM_AUTO = 4;
   public static final int GTM_SKIP = 0;
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
   DSGrayscaleTransformationModeInverted = 0x01
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   DSGrayscaleTransformationModeOriginal = 0x02
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   DSGrayscaleTransformationModeAuto     = 0x04
   /** Skips grayscale transformation. */
   DSGrayscaleTransformationModeSkip     = 0x00
   /** Reserved setting for grayscale transformation mode. */
   DSGrayscaleTransformationModeRev      = -2147483648
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
