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
```
>
```java
@IntDef({CB_IMAGE,CB_VIEW})
@Retention(RetentionPolicy.CLASS)
public @interface EnumCoordinateBase {
   // pixel, percentage
   public static final int CB_IMAGE = 0;
   // DP
   public static final int CB_VIEW = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSCoordinateBase) {
   /**
    * Image coordinate.
    */
   DSCoordinateBaseImage = 0,
   /**
    * View coordinate.
    */
   DSCoordinateBaseView = 1
};
```
>
```swift
public enum CoordinateBase : Int{
   /**
    * Image coordinate.
    */
   image = 0
   /**
    * View coordinate.
    */
   view = 1
}
```
