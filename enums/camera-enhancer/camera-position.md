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
   >- Android
   >- Objective-C
   >- Swift
   >
>
```java
public enum EnumCameraPosition {
   /** The back-facing camera. */
   CP_BACK(0),
   /** The front-facing camera. */
   CP_FRONT(1);
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSCameraPosition)
{
   /** The back-facing camera. */
   EnumCameraPositionBack = 0,
   /** The front-facing camera. */
   EnumCameraPositionBack = 1
};
```
>
```swift
public enum CameraPosition : Int{
   /** The back-facing camera. */
   back = 0
   /** The front-facing camera. */
   front = 1
}
```
