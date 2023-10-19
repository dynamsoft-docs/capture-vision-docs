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
@IntDef({DIS_DEFAULT,DIS_SELECTED})
@Retention(RetentionPolicy.CLASS)
public @interface EnumDrawingItemState {
   // The state of the DrawingItem is the default state.
   public static final int DIS_DEFAULT = 1;
   // The state of the DrawingItem is selected.
   public static final int DIS_SELECTED = 2;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSDrawingItemState) {
   /**
    * The state of the DrawingItem is the default state.
    */
   DSDrawingItemStateDefault = 1,
   /**
    * The state of the DrawingItem is selected.
    */
   DSDrawingItemStateSelected = 2
};
```
>
```swift
public enum CameraPosition : Int{
   /**
    * The state of the DrawingItem is the default state.
    */
   default = 1
   /**
    * The state of the DrawingItem is selected.
    */
   selected = 2
}
```
