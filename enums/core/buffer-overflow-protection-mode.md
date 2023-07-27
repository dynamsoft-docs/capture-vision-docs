---
layout: default-layout
Title: BufferOverflowProtectionMode - Dynamsoft Core Enumerations
Description: The enumeration BufferOverflowProtectionMode of Dynamsoft Core describes the protection modes when the buffer of ImageSourceAdapter is overflow.
Keywords: Buffer overflow protection mode 
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BufferOverflowProtectionMode
codeAutoHeight: true
---

# Enumeration BufferOverflowProtectionMode

`BufferOverflowProtectionMode` describes the protection modes when the buffer of `ImageSourceAdapter` is overflow.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumBufferOverflowProtectionMode {
   /** New images are blocked when the buffer is full.*/
   BOPM_Block = 0,
   /** New images are appended at the end, and oldest images are pushed out frombeginning if the buffer is full.*/
   BOPM_Append = 1
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumBufferOverflowProtectionMode
{
   /** New images are blocked when the buffer is full.*/
   public static final int BOPM_Block = 0;
   /** New images are appended at the end, and oldest images are pushed out from the beginning if thebuffer is full.*/
   public static final int BOPM_Append = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSBufferOverflowProtectionMode)
{
   /** New images are blocked when the buffer is full.*/
   DSBufferOverflowProtectionModeBlock = 0,
   /** New images are appended at the end, and oldest images are pushed out from the beginning if thebuffer is full.*/
   DSBufferOverflowProtectionModeAppend = 1,
};
```
>
```swift
public enum BufferOverflowProtectionMode : Int
{
   /** New images are blocked when the buffer is full.*/
   block = 0
   /** New images are appended at the end, and oldest images are pushed out from the beginning if thebuffer is full.*/
   append = 1
}
```
>
```cpp
typedef enum BufferOverflowProtectionMode
{
   /** New images are blocked when the buffer is full. */
   BOPM_BLOCK = 0,
   /** New images are appended at the end, and oldest images are pushed out from the beginning if the buffer is full. */
   BOPM_APPEND = 1
} BufferOverflowProtectionMode;
```
