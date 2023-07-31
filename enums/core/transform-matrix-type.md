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
    int TMT_LOCAL_TO_ORIGINAL_IMAGE = 0;
    int TMT_ORIGINAL_TO_LOCAL_IMAGE = 1;
    int TMT_ROTATED_TO_ORIGINAL_IMAGE = 2;
    int TMT_ORIGINAL_TO_ROTATED_IMAGE = 3;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSTransformMatrixType)
{
   DSTransformMatrixTypeLocalToOriginalImage = 0,
   DSTransformMatrixTypeOriginalToLocalImage = 1,
   DSTransformMatrixTypeRotatedToOriginalImage = 2,
   DSTransformMatrixTypeOriginalToRotatedImage = 3
}NS_SWIFT_NAME(TransformMatrixType);
```
>
```swift
public enum TransformMatrixType : Int
{
   localToOriginalImage = 0,
   originalToLocalImage = 1,
   rotatedToOriginalImage = 2,
   originalToRotatedImage = 3
}
```
>
```cpp
typedef enum TransformMatrixType
{
    TMT_LOCAL_TO_ORIGINAL_IMAGE,
    TMT_ORIGINAL_TO_LOCAL_IMAGE,
    TMT_ROTATED_TO_ORIGINAL_IMAGE,
    TMT_ORIGINAL_TO_ROTATED_IMAGE
} TransformMatrixType;
```
