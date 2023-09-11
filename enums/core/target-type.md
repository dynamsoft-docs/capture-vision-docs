---
layout: default-layout
title: TargetType - Dynamsoft Core Enumerations
description: The enumeration TargetType of Dynamsoft Core describes target types.
keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TargetType
codeAutoHeight: true
---

# Enumeration TargetType

`TargetType` describes the target types.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumTargetType
{
   /**The target type of the PDF file is "page". Only available for PDFReadingMode PDFRM_RASTER.*/
   TT_PAGE = 0,
   /**The target type of the PDF file is "image".*/
   TT_IMAGE = 1
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumTargetType {
   /**The target type of the PDF file is "page". Only available for PDFReadingMode raster.*/
   public static final int TT_PAGE = 0;
   /**The target type of the PDF file is "image".*/
   public static final int TT_IMAGE = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSTargetType)
{
   /**The target type of the PDF file is "page". Only available for PDFReadingMode raster.*/
   DSTargetTypePage = 0,
   /**The target type of the PDF file is "image".*/
   DSTargetTypeImage = 1
};
```
>
```swift
public enum TargetType : Int
{
   /**The target type of the PDF file is "page". Only available for PDFReadingMode raster.*/
   page = 0,
   /**The target type of the PDF file is "image".*/
   image = 1
}
```
>
```cpp
typedef enum TargetType
{
   /**The target type of the PDF file is "page". Only available for PDFReadingMode PDFRM_RASTER.*/
   TT_PAGE,
   /**The target type of the PDF file is "image".*/
   TT_IMAGE
} TargetType;
```
