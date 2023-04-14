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
public enum EnumFocusMode {
   // Lock the focal length.
   FM_LOCKED(1),
   // Keep continuous auto-focus.
   FM_CONTINUOUS_AUTO(2);
}
```
>
```objc
typedef NS_ENUM(NSInteger, EnumFocusMode)
{
   /** Lock the focal length. */
   FM_LOCKED = 1,
   /** Keep continuous auto-focus. */
   FM_CONTINUOUS_AUTO = 2
};
```
>
```swift
public enum EnumFocusMode : Int{
   /** Lock the focal length. */
   FM_LOCKED = 1
   /** Keep continuous auto-focus. */
   FM_CONTINUOUS_AUTO = 2
}
```
