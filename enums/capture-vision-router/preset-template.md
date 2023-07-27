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
enum PresetTemplate {
   /** Template name: "default". It implements barcode decoding, label recognizing and document normalizing. */
   PT_DEFAULT = 0,
   /** Template name: "read-barcodes". */
   PT_READ_BARCODES = 1,
   /** Template name: "recognize-textLines". */
   PT_RECOGNIZE_TEXT_LINES = 2,
   /** Template name: "detect-document-boundaries". */
   PT_DETECT_DOCUMENT_BOUNDARIES = 3,
   /** Template name: "detect-and-normalize-document". */
   PT_DETECT_AND_NORMALIZE_DOCUMENT = 4,
   /** Template name: "normalize-document". */
   PT_NORMALIZE_DOCUMENT = 5
}
```
>
```java
public class EnumPresetTemplate
{
   /** Template name: "default". It implements barcode decoding, label recognizing and document normalizing. */
   public static final int PT_DEFAULT = 0;
   /** Template name: "read-barcodes". */
   public static final int PT_READ_BARCODES = 1;
   /** Template name: "recognize-textLines". */
   public static final int PT_RECOGNIZE_TEXT_LINES = 2;
   /** Template name: "detect-document-boundaries". */
   public static final int PT_DETECT_DOCUMENT_BOUNDARIES = 3;
   /** Template name: "detect-and-normalize-document". */
   public static final int PT_DETECT_AND_NORMALIZE_DOCUMENT = 4;
   /** Template name: "normalize-document". */
   public static final int PT_NORMALIZE_DOCUMENT = 5;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSPresetTemplate)
{
   /** Template name: "default". It implements barcode decoding, label recognizing and document normalizing. */
   DSPresetTemplateDefault,
   /** Template name: "read-barcodes". */
   DSPresetTemplateReadBarcodes,
   /** Template name: "recognize-textLines". */
   DSPresetTemplateRecognizeTextLines,
   /** Template name: "detect-document-boundaries". */
   DSPresetTemplateDetectDocumentBoundaries,
   /** Template name: "detect-and-normalize-document". */
   DSPresetTemplateDetectAndNormalizeDocument,
   /** Template name: "normalize-document". */
   DSPresetTemplateNormalizeDocument
}NS_SWIFT_NAME(PresetTemplate);
```
>
```swift
public enum PresetTemplate : Int
{
   /** Template name: "default". It implements barcode decoding, label recognizing and document normalizing. */
   default
   /** Template name: "read-barcodes". */
   readBarcodes
   /** Template name: "recognize-textLines". */
   recognizeTextLines
   /** Template name: "detect-document-boundaries". */
   detectDocumentBoundaries
   /** Template name: "detect-and-normalize-document". */
   detectAndNormalizeDocument
   /** Template name: "normalize-document". */
   normalizeDocument
}
```
>
```cpp
typedef enum PresetTemplate {
   /** Template name: "default". It implements barcode decoding, label recognizing and document   normalizing. */
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
