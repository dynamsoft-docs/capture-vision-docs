---
layout: default-layout
Title: CornerType - Dynamsoft Core Enumerations
Description: The enumeration CornerType of Dynamsoft Core describes how the corner is formed by its sides.
Keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CornerType
---

# Enumeration CornerType

`CornerType` describes how the corner is formed by its sides.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C
   >- C++
   >- C#
   >- Java
   >- Python
   >
>
```javascript
```
>
```java
```
>
```objc
```
>
```swift
```
>
```c
```
>
```cpp
typedef enum CornerType
{
   /* The sides of the corner is normally intersected. */
   CT_NORMAL_INTERSECTED = 0,
   /* The sides of the corner is T-intersected. */
   CT_T_INTERSECTED = 1,
   /* The sides of the corner is cross-intersected. */
   CT_CROSS_INTERSECTED = 2,
   /* The sides are not intersected but they definitly make up a corner. */
   CT_NOT_INTERSECTED = 3,
} CornerType;
```
>
```csharp
```
>
```java
```
>
```python
```
