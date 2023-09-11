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

# Enumeration ImageSourceState

`ImageSourceState` describes the state of `ImageSourceAdapter`.

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
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   ISS_BUFFER_EMPTY = 0,
   /** The source of ImageSourceAdapter is empty. */
   ISS_EXHAUSTED = 1
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageSourceState
{
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   public static final int ISS_BUFFER_EMPTY = 0;
   /** The source of ImageSourceAdapter is empty. */
   public static final int ISS_EXHAUSTED = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSImageSourceState)
{
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   DSImageSourceStateBufferEmpty = 0,
   /** The source of ImageSourceAdapter is empty. */
   DSImageSourceStateExhausted = 1
};
```
>
```swift
public enum ImageSourceState : Int
{
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   bufferEmpty = 0
   /** The source of ImageSourceAdapter is empty. */
   exhausted = 1
};
```
>
```cpp
typedef enum ImageSourceState
{
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   ISS_BUFFER_EMPTY,
   /** The source of ImageSourceAdapter is empty. */
   ISS_EXHAUSTED
} ImageSourceState;
```
