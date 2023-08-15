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
   >- Android
   >- Objective-C
   >- Swift
   >
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumPresetTemplate
{
   /** Template name: "default". It implements barcode decoding, label recognizing and document normalizing. */
   String PT_DEFAULT = "default"; 
   /** Template name: "read-barcodes". */
   String PT_READ_BARCODES = "read-barcodes";
   /** Template name: "recognize-textLines". */
   String PT_RECOGNIZE_TEXT_LINES = "recognize-textlines";
   /** Template name: "detect-document-boundaries". */
   String PT_DETECT_DOCUMENT_BOUNDARIES = "detect-document-boundaries";
   /** Template name: "detect-and-normalize-document". */
   String PT_DETECT_AND_NORMALIZE_DOCUMENT = "detect-and-normalize-document";
   /** Template name: "normalize-document". */
   String PT_NORMALIZE_DOCUMENT = "normalize-document";
}
```
>
```objc
/**
 * DSPresetTemplate defines the enumerations that indicates the preset capture vision templates.
 */
typedef NSString * DSPresetTemplate NS_STRING_ENUM NS_SWIFT_NAME(PresetTemplate);
/**
 * The default template that performs barcode decoding, label recognizing, boundary detecting and document normalizing. The template name is "default".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateDefault NS_SWIFT_NAME(presetDefault);
/**
 * The template that enables barcode decoding only. The template name is "read-barcodes".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateReadBarcodes NS_SWIFT_NAME(readBarcodes);
/**
 * The template that enables label recognizing only. The template name is "recognize-textLines".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateRecognizeTextLines NS_SWIFT_NAME(recognizeTextLines);
/**
 * The template that enables boundary detecting only. The template name is "detect-document-boundaries".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateDetectDocumentBoundaries NS_SWIFT_NAME(detectDocumentBoundaries);
/**
 * The template that enables both boundary detecting and document normalizing. The template name is "detect-and-normalize-document".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateDetectAndNormalizeDocument NS_SWIFT_NAME(detectAndNormalizeDocument);
/**
 * The template that enables document normalizing only. The template name is "normalize-document".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateNormalizeDocument NS_SWIFT_NAME(normalizeDocument);
```
>
```swift
struct PresetTemplate
{
   /** Template name: "default". It implements barcode decoding, label recognizing and document normalizing. */
   static let default = "default";
   /** Template name: "read-barcodes". */
    static let readBarcodes = "read-barcodes";
   /** Template name: "recognize-textLines". */
    static let recognizeTextLines = "recognize-textLines";
   /** Template name: "detect-document-boundaries". */
    static let detectDocumentBoundaries = "detect-document-boundaries";
   /** Template name: "detect-and-normalize-document". */
    static let detectAndNormalizeDocument ="detect-and-normalize-document";
   /** Template name: "normalize-document". */
    static let normalizeDocument="normalize-document";
}
```
