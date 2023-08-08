---
layout: default-layout
Title: TransformMatrixType - Dynamsoft Core Enumerations
Description: The enumeration TransformMatrixType of Dynamsoft Core describes transform matrix types.
Keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TransformMatrixType
---

# Enumeration TransformMatrixType

`TransformMatrixType` describes the target types.

<div class="sample-code-prefix template2"></div>
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
>
```java
public @interface EnumTransformMatrixType {
    /**Represents a transformation matrix that converts coordinates from the local image to the original image.*/
    int TMT_LOCAL_TO_ORIGINAL_IMAGE = 0;
    /**Represents a transformation matrix that converts coordinates from the original image to the local image.*/
    int TMT_ORIGINAL_TO_LOCAL_IMAGE = 1;
    /**Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
    int TMT_ROTATED_TO_ORIGINAL_IMAGE = 2;
    /**Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
    int TMT_ORIGINAL_TO_ROTATED_IMAGE = 3;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSTransformMatrixType)
{
    /**Represents a transformation matrix that converts coordinates from the local image to the original image.*/
   DSTransformMatrixTypeLocalToOriginalImage = 0,
    /**Represents a transformation matrix that converts coordinates from the original image to the local image.*/
   DSTransformMatrixTypeOriginalToLocalImage = 1,
    /**Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
   DSTransformMatrixTypeRotatedToOriginalImage = 2,
    /**Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
   DSTransformMatrixTypeOriginalToRotatedImage = 3
}NS_SWIFT_NAME(TransformMatrixType);
```
>
```swift
public enum TransformMatrixType : Int
{
    /**Represents a transformation matrix that converts coordinates from the local image to the original image.*/
   localToOriginalImage = 0,
    /**Represents a transformation matrix that converts coordinates from the original image to the local image.*/
   originalToLocalImage = 1,
    /**Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
   rotatedToOriginalImage = 2,
    /**Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
   originalToRotatedImage = 3
}
```
>
```cpp
typedef enum TransformMatrixType
{
    /**Represents a transformation matrix that converts coordinates from the local image to the original image.*/
    TMT_LOCAL_TO_ORIGINAL_IMAGE,
    /**Represents a transformation matrix that converts coordinates from the original image to the local image.*/
    TMT_ORIGINAL_TO_LOCAL_IMAGE,
    /**Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
    TMT_ROTATED_TO_ORIGINAL_IMAGE,
    /**Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
    TMT_ORIGINAL_TO_ROTATED_IMAGE
} TransformMatrixType;
```