---
layout: default-layout
title: FocusMode - Dynamsoft Camera Enhancer Enumerations
description: The enumeration FocusMode of Dynamsoft Camera Enhancer describes the focus mode.
keywords:  Focus mode
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: FocusMode
---

# FocusMode

Enumeration `FocusMode` describes the focus mode.

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
@IntDef({FM_LOCKED,FM_CONTINUOUS_AUTO})
@Retention(RetentionPolicy.CLASS)
public @interface EnumFocusMode {
   // Lock the focal length.
   public static final int FM_LOCKED = 1;
   // Keep continuous auto-focus.
   public static final int FM_CONTINUOUS_AUTO = 2;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSFocusMode){
   /**
    * Lock the focal length.
    */
   FocusModeLocked           =   1,
   /**
    * Enable the continuous auto-focus.
    */
   FocusModeContinuousAuto     =   2
};
```
>
```swift
public enum FocusMode : Int{
   /**
    * Lock the focal length.
    */
   locked           =   1
   /**
    * Enable the continuous auto-focus.
    */
   continuousAuto     =   2
}
```
