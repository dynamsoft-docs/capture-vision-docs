---
layout: default-layout
Title: CaptureState - Dynamsoft Vision Router Enumerations
Description: The enumeration CaptureState of Dynamsoft Vision Router describes the state of data capturing.
Keywords: Capture state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CaptureState
---

# Enumeration CaptureState

`CaptureState` describes the state of data capturing.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumCaptureState
{
   /** The data capturing is started. */
   CS_STARTED = 0,
   /** The data capturing is stopped. */
   CS_STOPPED = 1
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumCaptureState
{
   /** The data capturing is started. */
   public static final int CS_STARTED = 0;
   /** The data capturing is stopped. */
   public static final int CS_STOPPED = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSCaptureState)
{
   /** The data capturing is started. */
   DSCaptureStateStarted,
   /** The data capturing is stopped. */
   DSCaptureStateStopped
};
```
>
```swift
public enum CaptureState : Int
{
   /** The data capturing is started. */
   started
   /** The data capturing is stopped. */
   stopped
};
```
>
```cpp
typedef enum CaptureState
{
   /** The data capturing is started. */
   CS_STARTED,
   /** The data capturing is stopped. */
   CS_STOPPED
} CaptureState;
```
