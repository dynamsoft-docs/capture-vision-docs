---
layout: default-layout
title: BufferOverflowProtectionMode - Dynamsoft Core Enumerations
description: The enumeration BufferOverflowProtectionMode of Dynamsoft Core describes the protection modes when the buffer of ImageSourceAdapter is overflow.
keywords: Buffer overflow protection mode 
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BufferOverflowProtectionMode
codeAutoHeight: true
---

# Enumeration BufferOverflowProtectionMode

`BufferOverflowProtectionMode` describes the protection modes to manage situations when the `ImageSourceAdapter`'s buffer exceeds its capacity. 

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >- C#
   >- Python
   >
>
```javascript
enum EnumBufferOverflowProtectionMode {
   /** New images are blocked when the buffer is full.*/
   BOPM_Block = 0,
   /** New images are appended at the end, and oldest images are pushed out from the beginning if the buffer is full.*/
   BOPM_Update = 1
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumBufferOverflowProtectionMode
{
   /** New images are blocked when the buffer is full.*/
   public static final int BOPM_BLOCK = 0;
   /** New images are appended at the end, and oldest images are pushed out from the beginning if thebuffer is full.*/
   public static final int BOPM_UPDATE = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSBufferOverflowProtectionMode)
{
   /** New images are blocked when the buffer is full.*/
   DSBufferOverflowProtectionModeBlock = 0,
   /** New images are appended at the end, and oldest images are pushed out from the beginning if thebuffer is full.*/
   DSBufferOverflowProtectionModeUpdate = 1,
}NS_SWIFT_NAME(BufferOverflowProtectionMode);
```
>
```swift
public enum BufferOverflowProtectionMode : Int
{
   /** New images are blocked when the buffer is full.*/
   block = 0
   /** New images are appended at the end, and oldest images are pushed out from the beginning if thebuffer is full.*/
   update = 1
}
```
>
```cpp
typedef enum BufferOverflowProtectionMode
{
   /** New images are blocked when the buffer is full. */
   BOPM_BLOCK = 0,
   /** New images are appended at the end, and oldest images are pushed out from the beginning if the buffer is full. */
   BOPM_UPDATE = 1
} BufferOverflowProtectionMode;
```
>
```csharp
public enum EnumBufferOverflowProtectionMode
{
    /** New images are blocked when the buffer is full. */
    BOPM_BLOCK = 0x00,
    /** New images are appended at the end, and the oldest images are pushed out from the beginning if the buffer is full. */
    BOPM_UPDATE = 0x01,
}
```
>
```python
class EnumBufferOverflowProtectionMode(IntEnum):
    # New images are blocked when the buffer is full. 
    BOPM_BLOCK = 0x00
    # New images are appended at the end, and the oldest images are pushed out from the beginning if the buffer is full. 
    BOPM_UPDATE = 0x01
```
