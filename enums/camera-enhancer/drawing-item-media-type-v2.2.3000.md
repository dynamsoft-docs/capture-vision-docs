---
layout: default-layout
title: CameraPosition - Dynamsoft Camera Enhancer Enumerations
description: The enumeration CameraPosition of Dynamsoft Camera Enhancer describes the camera position.
keywords:  Camera Position
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CameraPosition
---

# CameraPosition

Enumeration `CameraPosition` describes the camera position.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >
>
```javascript
enum EnumDrawingItemMediaType {
   /**The mediate type of the DrawingItem is rectangle. */
   DIMT_RECTANGLE = 1,
   /**The mediate type of the DrawingItem is quadrilateral. */
   DIMT_QUADRILATERAL = 2,
   /**The mediate type of the DrawingItem is text. */
   DIMT_TEXT = 4,
   /**The mediate type of the DrawingItem is arc. */
   DIMT_ARC = 8,
   /**The mediate type of the DrawingItem is image. */
   DIMT_IMAGE = 16,
   /**The mediate type of the DrawingItem is polygon. */
   DIMT_POLYGON = 32,
   /**The mediate type of the DrawingItem is line. */
   DIMT_LINE = 64,
   /**The mediate type of the DrawingItem is a group of shapes. */
   DIMT_GROUP = 128
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumDrawingItemMediaType {
   // The mediate type of the DrawingItem is rectangle.
   public static final int DIMT_RECTANGLE = 1;
   // The mediate type of the DrawingItem is quadrilateral.
   public static final int DIMT_QUADRILATERAL = 2;
   // The mediate type of the DrawingItem is text.
   public static final int DIMT_TEXT = 4;
   // The mediate type of the DrawingItem is line.
   public static final int DIMT_LINE = 8;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSDrawingItemMediaType) {
   /**
    * The mediate type of the DrawingItem is rectangle.
    */
   DSDrawingItemMediaTypeRectangle = 1,
   /**
    * The mediate type of the DrawingItem is quadrilateral.
    */
   DSDrawingItemMediaTypeQuadrilateral = 2,
   /**
    * The mediate type of the DrawingItem is text.
    */
   DSDrawingItemMediaTypeText = 4,
   /**
    * The mediate type of the DrawingItem is line.
    */
   DSDrawingItemMediaTypeLine = 8
};
```
>
```swift
public enum DrawingItemMediaType : Int{
   /**
    * The mediate type of the DrawingItem is rectangle.
    */
   rectangle = 1
   /**
    * The mediate type of the DrawingItem is quadrilateral.
    */
   quadrilateral = 2
   /**
    * The mediate type of the DrawingItem is text.
    */
   text = 4
   /**
    * The mediate type of the DrawingItem is line.
    */
   line = 8
}
```
