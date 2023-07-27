---
layout: default-layout
Title: ImageTagType - Dynamsoft Core Enumerations
Description: The enumeration ImageTagType of Dynamsoft Core describes the types of image tags.
Keywords: Image tag type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageTagType
codeAutoHeight: true
---

# Enumeration ImageTagType

`ImageTagType` describes the type of the image tag, which is used to distinguish video frame and file images.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumImageTagType
{
   /**The image is a file image.*/
   ITT_FILE_IMAGE = 0,
   /**The image is a video frame.*/
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
   /**The image is a file image.*/
   ITT_FILE_IMAGE,
   /**The image is a video frame.*/
   ITT_VIDEO_FRAME
} ImageTagType;
```
