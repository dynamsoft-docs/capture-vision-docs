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
@IntDef({OPENING,OPENED,CLOSING,CLOSED})
@Retention(RetentionPolicy.CLASS)
public @interface EnumCameraState {
   // The camera is opening.
   public static final int OPENING = 0;
   // The camera is opened.
   public static final int OPENED = 1;
   // The camera is closing.
   public static final int CLOSING = 2;
   // The camera is closed.
   public static final int CLOSED = 3;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSCameraState)
{
   /**
    * The camera is opening.
    */
   CameraStateOpening = 0,
   /**
    * The camera is opened.
    */
   CameraStateOpened = 1,
   /**
    * The camera is closing.
    */
   CameraStateClosing = 2,
   /**
    * The camera is closed.
    */
   CameraStateClosed = 3
};
```
>
```swift
public enum CameraState : Int{
   /**
    * The camera is opening.
    */
   opening = 0
   /**
    * The camera is opened.
    */
   opened = 1
   /**
    * The camera is closing.
    */
   closing = 2
   /**
    * The camera is closed.
    */
   closed = 3
}
```
