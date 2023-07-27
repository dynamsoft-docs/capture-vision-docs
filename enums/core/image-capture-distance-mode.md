---
layout: default-layout
Title: ImageCaptureDistanceMode - Dynamsoft Core Enumerations
Description: The enumeration ImageCaptureDistanceMode of Dynamsoft Core is used to distinguish the close-up images from the prospect images.
Keywords: Image capture distance
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageCaptureDistanceMode
---

# Enumeration ImageCaptureDistanceMode

`ImageCaptureDistanceMode` describes the shooting mode of the image. It is used in the `overlap` mode of `Panorama`.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum ImageCaptureDistanceMode
{
   /** The image is taken by close-up shot camera. */
   ICDM_NEAR = 0,
   /** The image is taken by long shot camera. */
   ICDM_FAR = 1
}
```
>
```java
public class EnumImageCaptureDistanceMode
{
   /** The image is taken by close-up shot camera. */
   public static final int ICDM_NEAR = 0;
   /** The image is taken by long shot camera. */
   public static final int ICDM_FAR = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSImageCaptureDistanceMode)
{
   /** The image is taken by close-up shot camera. */
   DSImageCaptureDistanceModeNear,
   /** The image is taken by long shot camera. */
   DSImageCaptureDistanceModeFar
}NS_SWIFT_NAME(ImageCaptureDistanceMode);
```
>
```swift
public enum ImageCaptureDistanceMode : Int
{
   /** The image is taken by close-up shot camera. */
   near
   /** The image is taken by long shot camera. */
   far
}
```
>
```cpp
typedef enum ImageCaptureDistanceMode
{
   /** The image is taken by close-up shot camera. */
   ICDM_NEAR,
   /** The image is taken by long shot camera. */
   ICDM_FAR
} CaptureDistanceMode;
```
