---
layout: default-layout
title: ImageCaptureDistanceMode - Dynamsoft Core Enumerations
description: The enumeration ImageCaptureDistanceMode of Dynamsoft Core is used to distinguish the close-up images from the prospect images.
keywords: Image capture distance
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageCaptureDistanceMode
codeAutoHeight: true
---

# Enumeration ImageCaptureDistanceMode

`ImageCaptureDistanceMode` describes the shooting mode of the image. It is used in the `overlap` mode of `Panorama`.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >- C#
   >- Python
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
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageCaptureDistanceMode
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
};
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
>
```csharp
public enum EnumImageCaptureDistanceMode
{
    /**The image is taken by close-up shot camera.*/
    ICDM_NEAR,
    /**The image is taken by long shot camera.*/
    ICDM_FAR
}
```
>
```python
class EnumImageCaptureDistanceMode(IntEnum):
    #The image is taken by close-up shot camera.
    ICDM_NEAR
    #The image is taken by long shot camera.
    ICDM_FAR
```
