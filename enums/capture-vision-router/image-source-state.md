---
layout: default-layout
title: ImageSourceState - Dynamsoft Core Enumerations
description: The enumeration ImageSourceState of Dynamsoft Core describes the state of ImageSourceAdapter.
keywords: Image source state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageSourceState
codeAutoHeight: true
---
<!--Moved from Core to CVR in May 2023-->

# Enumeration ImageSourceState

`ImageSourceState` describes the status of an object that conforms to the `ImageSourceAdapter` interface and is designated as the image source in a `CaptureVisionRouter` object.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumImageSourceState
{
   /** Indicates that the buffer of the image source is currently empty. */
   ISS_BUFFER_EMPTY = 0,
   /** Signifies that the source for the image source has been depleted. */
   ISS_EXHAUSTED = 1
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageSourceState
{
   /** Indicates that the buffer of the image source is currently empty. */
   public static final int ISS_BUFFER_EMPTY = 0;
   /** Signifies that the source for the image source has been depleted. */
   public static final int ISS_EXHAUSTED = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSImageSourceState)
{
   /** Indicates that the buffer of the image source is currently empty. */
   DSImageSourceStateBufferEmpty = 0,
   /** Signifies that the source for the image source has been depleted. */
   DSImageSourceStateExhausted = 1
};
```
>
```swift
public enum ImageSourceState : Int
{
   /** Indicates that the buffer of the image source is currently empty. */
   bufferEmpty = 0
   /** Signifies that the source for the image source has been depleted. */
   exhausted = 1
};
```
>
```cpp
typedef enum ImageSourceState
{
   /** Indicates that the buffer of the image source is currently empty. */
   ISS_BUFFER_EMPTY,
   /** Signifies that the source for the image source has been depleted. */
   ISS_EXHAUSTED
} ImageSourceState;
```
