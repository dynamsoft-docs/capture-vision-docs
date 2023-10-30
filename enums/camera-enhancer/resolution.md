---
layout: default-layout
title: Resolution - Dynamsoft Camera Enhancer Enumerations
description: The enumeration Resolution of Dynamsoft Camera Enhancer describes the resolution.
keywords:  Resolution
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: Resolution
---

# EnumResolution

Enumeration `Resolution` describes the resolution.

<div class="sample-code-prefix template2"></div>
   >- Android
   >- Objective-C
   >- Swift
   >
>
```java
@IntDef({RESOLUTION_AUTO,RESOLUTION_480P,RESOLUTION_720P,RESOLUTION_1080P,RESOLUTION_2K,RESOLUTION_4K})
@Retention(RetentionPolicy.CLASS)
public @interface EnumResolution {
   // Auto choose resolution, expected 1080P, if can't choose, choose first lower than 1080P.
   public static final int RESOLUTION_AUTO = 0;
   // 480P
   public static final int RESOLUTION_480P = 1;
   // 720P
   public static final int RESOLUTION_720P = 2;
   // 1080P
   public static final int RESOLUTION_1080P = 3;
   // 2K
   public static final int RESOLUTION_2K = 4;
   // 4K
   public static final int RESOLUTION_4K = 5;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSResolution)
{
   /**
    * Set the video streaming to the auto selected resolution.
    */
   ResolutionAuto = 0,
   /**
    * Set the video streaming to the 480P resolution.
    */
   Resolution480P = 1,
   /**
    * Set the video streaming to the 720P resolution.
    */
   Resolution720P = 2,
   /**
    * Set the video streaming to the 480P resolution.
    */
   Resolution1080P = 3,
   /**
    * Set the video streaming to the 4K resolution.
    */
   Resolution4K = 4
};
```
>
```swift
public enum Resolution : Int{
   /**
    * Set the video streaming to the auto selected resolution.
    */
   auto = 0
   /**
    * Set the video streaming to the 480P resolution.
    */
   480P = 1
   /**
    * Set the video streaming to the 720P resolution.
    */
   720P = 2
   /**
    * Set the video streaming to the 480P resolution.
    */
   1080P = 3
   /**
    * Set the video streaming to the 4K resolution.
    */
   4K = 4
}
```
