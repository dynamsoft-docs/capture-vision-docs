---
layout: default-layout
title: CameraState - Dynamsoft Camera Enhancer Enumerations
description: The enumeration CameraState of Dynamsoft Camera Enhancer describes the camera state.
keywords:  Camera state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CameraState
---

# CameraState

Enumeration `CameraState` describes the camera state.

<div class="sample-code-prefix template2"></div>
   >- Android
   >- Objective-C
   >- Swift
   >
>
```java
public enum EnumCameraState {
   OPENING(0),
   OPENED(1),
   CLOSING(2),
   CLOSED(3);
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSCameraState)
{
   /** The camera is opening.*/
   EnumCAMERA_STATE_OPENING NS_SWIFT_NAME(EnumCAMERA_STATE_OPENING)  = 0,
   /** The camera is opened.*/
   EnumCAMERA_STATE_OPENED  NS_SWIFT_NAME(EnumCAMERA_STATE_OPENED)   = 1,
   /** The camera is closing.*/
   EnumCAMERA_STATE_CLOSING  NS_SWIFT_NAME(EnumCAMERA_STATE_CLOSING)   = 2,
   /** The camera is closed.*/
   EnumCAMERA_STATE_CLOSED  NS_SWIFT_NAME(EnumCAMERA_STATE_CLOSED)   = 3
};
```
>
```swift
public enum EnumCameraState : Int{
   /** The camera is opening.*/
   EnumCAMERA_STATE_OPENING = 0
   /** The camera is opened.*/
   EnumCAMERA_STATE_OPENED = 1
   /** The camera is closing.*/
   EnumCAMERA_STATE_CLOSING = 2
   /** The camera is closed.*/
   EnumCAMERA_STATE_CLOSED = 3
}
```
