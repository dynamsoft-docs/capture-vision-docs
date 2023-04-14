---
layout: default-layout
Title: SectionType - Dynamsoft Core Enumerations
Description: The enumeration SectionType of Dynamsoft Core describes the section of the algorithm.
Keywords: Section type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: SectionType
---

# Enumeration SectionType

`SectionType` describes the section of the algorithm. In the `IntermediateResultReceiver`, the `SectionType` indicate the algorithm section that produced the `IntermediateResult`.

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
typedef enum SectionType
{
   /** The result is output by "region prediction" section. */
   ST_REGION_PREDETECTION,
   /** The result is output by "barcode localization" section. */
   ST_BARCODE_LOCALIZATION,
   /** The result is output by "barcode decoding" section. */
   ST_BARCODE_DECODING,
   /** The result is output by "text line localization" section. */
   ST_TEXT_LINE_LOCALIZATION,
   /** The result is output by "text line  recognition" section. */
   ST_TEXT_LINE_RECOGNITION,
   /** The result is output by "document detection" section. */
   ST_DOCUMENT_DETECTION,
   /** The result is output by "document normalization" section. */
   ST_DOCUMENT_NORMALIZATION,
} SectionType;
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
