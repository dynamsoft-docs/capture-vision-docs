---
layout: default-layout
title: VideoFrameQuality - Dynamsoft Core Enumerations
description: The enumeration VideoFrameQuality of Dynamsoft Core describes the quality of video frames.
keywords: Video frame quality
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: VideoFrameQuality
codeAutoHeight: true
---

# Enumeration VideoFrameQuality

`VideoFrameQuality` describes the quality of video frames.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumVideoFrameQuality {
   /**The frame quality is measured to be high.*/
   VFQ_HIGH = 0,
   /**The frame quality is measured to be low.*/
   VFQ_LOW = 1,
   /**The frame quality is unknown.*/
   VFQ_UNKNOWN = 2
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumVideoFrameQuality {
   /**The frame quality is measured to be high.*/
   public static final int VFQ_HIGH = 0;
   /**The frame quality is measured to be low.*/
   public static final int VFQ_LOW = 1;
   /**The frame quality is unknown.*/
   public static final int VFQ_UNKNOWN = 2;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSVideoFrameQuality)
{
   /**The frame quality is measured to be high.*/
   VideoFrameQualityHigh,
   /**The frame quality is measured to be low.*/
   VideoFrameQualityLow,
   /**The frame quality is unknown.*/
   VideoFrameQualityUnknown
};
```
>
```swift
public enum VideoFrameQuality : Int
{
   /**The frame quality is measured to be high.*/
   high,
   /**The frame quality is measured to be low.*/
   low,
   /**The frame quality is unknown.*/
   unknown
}
```
>
```cpp
typedef enum VideoFrameQuality {
   /**The frame quality is measured to be high.*/
   VFQ_HIGH,
   /**The frame quality is measured to be low.*/
   VFQ_LOW,
   /**The frame quality is unknown.*/
   VFQ_UNKNOWN
} VideoFrameQuality;
```
