---
layout: default-layout
Title: RegionObjectElementType - Dynamsoft Core Enumerations
Description: The enumeration RegionObjectElementType of Dynamsoft Core describes the types of RegionObjectElement.
Keywords: Region object element type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RegionObjectElementType
---

# Enumeration RegionObjectElementType

`RegionObjectElementType` is used to determine the particular type of the subclasses of `RegionOjectElement`.

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
typedef enum RegionObjectElementType
{
   /** The type of subclass PredetectedRegionElement. */
   ROET_PREDETECTED_REGION,
   /** The type of subclass LocalizedBarcodeElement. */
   ROET_LOCALIZED_BARCODE,
   /** The type of subclass PredetectedRegionElement. */
   ROET_DECODED_BARCODE,
   /** The type of subclass LocalizedTextLineElement. */
   ROET_LOCALIZED_TEXT_LINE,
   /** The type of subclass RecognizedTextLineElement. */
   ROET_RECOGNIZED_TEXT_LINE,
   /** The type of subclass DetectedQuadElement. */
   ROET_DETECTED_QUAD,
   /** The type of subclass NormalizedImageElement. */
   ROET_NORMALIZED_IMAGE,
   /** The type of subclass SourceImageElement. */
   ROET_SOURCE_IMAGE,
   /** The type of subclass TargetROIElement. */
   ROET_TARGET_ROI
} RegionObjectElementType;
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
