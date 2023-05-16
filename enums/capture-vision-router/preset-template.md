---
layout: default-layout
Title: PresetTemplate - Dynamsoft Vision Router Enumerations
Description: The enumeration PresetTemplate of Dynamsoft Vision Router describes the preset template.
Keywords: Capture state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: PresetTemplate
---

# Enumeration PresetTemplate

`PresetTemplate` describes the state of data capturing.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
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
```cpp
typedef enum PresetTemplate {
    /** Template name: "default". It implements barcode decoding, label recognizing and document normalizing. */
    PT_DEFAULT,
    /** Template name: "read-barcodes". */
    PT_READ_BARCODES,
    /** Template name: "recognize-textLines". */
    PT_RECOGNIZE_TEXT_LINES,
    /** Template name: "detect-document-boundaries". */
    PT_DETECT_DOCUMENT_BOUNDARIES,
    /** Template name: "detect-and-normalize-document". */
    PT_DETECT_AND_NORMALIZE_DOCUMENT,
    /** Template name: "normalize-document". */
    PT_NORMALIZE_DOCUMENT
} PresetTemplate;
```
