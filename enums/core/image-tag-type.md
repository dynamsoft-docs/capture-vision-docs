---
layout: default-layout
title: ImageTagType - Dynamsoft Core Enumerations
description: The enumeration ImageTagType of Dynamsoft Core describes the types of image tags.
keywords: Image tag type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageTagType
codeAutoHeight: true
---

# Enumeration ImageTagType

`ImageTagType` categorizes images based on their source, distinguishing between images extracted from video streams (video frame) and those loaded from static files (file image).

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
enum EnumImageTagType
{
   /**Represents an image that has been sourced from a static file.*/
   ITT_FILE_IMAGE = 0,
   /**Indicates that the image is a frame extracted from a video stream.*/
   ITT_VIDEO_FRAME = 1
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageTagType
{
   public static final int ITT_FILE_IMAGE = 0;
   public static final int ITT_VIDEO_FRAME = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSImageTagType)
{
   /**The image tag is a DSFileImageTag.*/
   DSImageTagTypeFileImage = 0,
   /**The image tag is a DSVideoFrameTag.*/
   DSImageTagTypeVideoFrame = 1,
};
```
>
```swift
public enum ImageTagType : Int
{
   /**The image tag is a DSFileImageTag.*/
   fileImage = 0,
   /**The image tag is a DSVideoFrameTag.*/
   videoFrame = 1,
}
```
>
```cpp
typedef enum ImageTagType
{
   /**Represents an image that has been sourced from a static file.*/
   ITT_FILE_IMAGE,
   /**Indicates that the image is a frame extracted from a video stream.*/
   ITT_VIDEO_FRAME
} ImageTagType;
```
>
```csharp
public enum EnumImageTagType
{
    /**The image is a file image.*/
    ITT_FILE_IMAGE,
    /**The image is a video frame.*/
    ITT_VIDEO_FRAME
}
```
>
```python
class EnumImageTagType(IntEnum):
    #The image is a file image.
    ITT_FILE_IMAGE
    #The image is a video frame.
    ITT_VIDEO_FRAME
```
