---
layout: default-layout
title: PresetTemplate - Dynamsoft Vision Router Enumerations
description: The enumeration PresetTemplate of Dynamsoft Vision Router describes the preset template.
keywords: Capture state
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
   /** Template name: "Default". It implements barcode decoding, label recognizing and document normalizing. */
   String PT_DEFAULT = "Default";
   /** Template name: "ReadBarcodes_Default". */
   String PT_READ_BARCODES = "ReadBarcodes_Default";
   /** Template name: "RecognizeTextLines_Default". */
   String PT_RECOGNIZE_TEXT_LINES = "RecognizeTextLines_Default";
   /** Template name: "DetectDocumentBoundaries_Default". */
   String PT_DETECT_DOCUMENT_BOUNDARIES = "DetectDocumentBoundaries_Default";
   /** Template name: "DetectAndNormalizeDocument_Default". */
   String PT_DETECT_AND_NORMALIZE_DOCUMENT = "DetectAndNormalizeDocument_Default";
   /** Template name: "NormalizeDocument_Default". */
   String PT_NORMALIZE_DOCUMENT = "NormalizeDocument_Default";
   /** Template name: "ReadBarcodes_SpeedFirst". */
   String PT_READ_BARCODES_SPEED_FIRST = "ReadBarcodes_SpeedFirst";
   /** Template name: "ReadBarcodes_ReadRateFirst". */
   String PT_READ_BARCODES_READ_RATE_FIRST = "ReadBarcodes_ReadRateFirst";
   /** Template name: "ReadSingleBarcode". */
   String PT_READ_SINGLE_BARCODE = "ReadSingleBarcode";
   /** Template name: "RecognizeNumbers". */
   String PT_RECOGNIZE_NUMBERS = "RecognizeNumbers";
   /** Template name: "RecognizeLetters". */
   String PT_RECOGNIZE_LETTERS = "RecognizeLetters";
   /** Template name: "RecognizeNumbersAndLetters". */
   String PT_RECOGNIZE_NUMBERS_AND_LETTERS = "RecognizeNumbersAndLetters";
   /** Template name: "RecognizeNumbersAndUppercaseLetters". */
   String PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS = "RecognizeNumbersAndUppercaseLetters";
   /** Template name: "RecognizeUppercaseLetters". */
   String PT_RECOGNIZE_UPPERCASE_LETTERS = "RecognizeUppercaseLetters";
}
```
>
```objc
/**
 * DSPresetTemplate defines the enumerations that indicates the preset capture vision templates.
 */
typedef NSString * DSPresetTemplate NS_STRING_ENUM NS_SWIFT_NAME(PresetTemplate);
/**
 * The default template that performs barcode decoding, label recognizing, boundary detecting and document normalizing. The template name is "Default".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateDefault NS_SWIFT_NAME(presetDefault);
/**
 * The template that enables barcode decoding only. The template name is "ReadBarcodes_Default".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateReadBarcodes NS_SWIFT_NAME(readBarcodes);
/**
 * The template that enables label recognizing only. The template name is "RecognizeTextLines_Default".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateRecognizeTextLines NS_SWIFT_NAME(recognizeTextLines);
/**
 * The template that enables boundary detecting only. The template name is "DetectDocumentBoundaries_Default".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateDetectDocumentBoundaries NS_SWIFT_NAME(detectDocumentBoundaries);
/**
 * The template that enables both boundary detecting and document normalizing. The template name is "DetectAndNormalizeDocument_Default".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateDetectAndNormalizeDocument NS_SWIFT_NAME(detectAndNormalizeDocument);
/**
 * The template that enables document normalizing only. The template name is "NormalizeDocument_Default".
 */
FOUNDATION_EXPORT DSPresetTemplate const _Nonnull DSPresetTemplateNormalizeDocument NS_SWIFT_NAME(normalizeDocument);
/**
 * The template that enables barcode decoding and the speed performance is prioritized. The template name is "ReadBarcodes_SpeedFirst".
 */
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateReadBarcodesSpeedFirst NS_SWIFT_NAME(readBarcodesSpeedFirst);
/**
 * The template that enables barcode decoding and the read rate performance is prioritized. The template name is "ReadBarcodes_ReadRateFirst"
 */
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateReadBarcodesReadRateFirst NS_SWIFT_NAME(readBarcodesReadRateFirst);
/**
 * This template is specially configured for single barcode decoding. The template name is "ReadSingleBarcode"
 */
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateReadSingleBarcode NS_SWIFT_NAME(readSingleBarcode);
/**
 * This template is specially configured for recognizing numbers from the text lines. The template name is "RecognizeNumbers"
 */
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeNumbers NS_SWIFT_NAME(recognizeNumbers);
/**
 * This template is specially configured for recognizing letters from the text lines. The template name is "RecognizeLetters"
 */
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeLetters NS_SWIFT_NAME(recognizeLetters);
/**
 * This template is specially configured for recognizing number and letters from the text lines. The template name is "RecognizeNumbersAndLetters"
 */
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeNumbersAndLetters NS_SWIFT_NAME(recognizeNumbersAndLetters);
/**
 * This template is specially configured for recognizing number and upper case letters from the text lines. The template name is "RecognizeNumbersAndUppercaseLetters"
 */
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeNumbersAndUppercaseLetters NS_SWIFT_NAME(recognizeNumbersAndUppercaseLetters);
/**
 * This template is specially configured for recognizing upper case letters from the text lines. The template name is "RecognizeUppercaseLetters"
 */
FOUNDATION_EXPORT PresetTemplate const _Nonnull DSPresetTemplateRecognizeUppercaseLetters NS_SWIFT_NAME(recognizeUppercaseLetters);
```
>
```swift
struct PresetTemplate
{
   /**
    * The default template that performs barcode decoding, label recognizing, boundary detecting and document normalizing. The template name is "Default".
    */
   static let default = "default"
   /**
    * The template that enables barcode decoding only. The template name is "ReadBarcodes_Default".
    */
   static let readBarcodes = "read-barcodes"
   /**
    * The template that enables label recognizing only. The template name is "RecognizeTextLines_Default".
    */
   static let recognizeTextLines = "recognize-textLines"
   /**
    * The template that enables boundary detecting only. The template name is "DetectDocumentBoundaries_Default".
    */
   static let detectDocumentBoundaries = "detect-document-boundaries"
   /**
    * The template that enables both boundary detecting and document normalizing. The template name is "DetectAndNormalizeDocument_Default".
    */
   static let detectAndNormalizeDocument = "DetectAndNormalizeDocument_Default"
   /**
    * The template that enables document normalizing only. The template name is "NormalizeDocument_Default".
    */
   static let normalizeDocument = "NormalizeDocument_Default"
   /**
    * The template that enables barcode decoding and the speed performance is prioritized. The template name is "ReadBarcodes_SpeedFirst".
    */
   static let readBarcodesSpeedFirst = "ReadBarcodes_SpeedFirst"
   /**
    * The template that enables barcode decoding and the read rate performance is prioritized. The template name is "ReadBarcodes_ReadRateFirst".
    */
   static let readBarcodesReadRateFirst = "ReadBarcodes_ReadRateFirst"
   /**
    * This template is specially configured for single barcode decoding. The template name is "ReadSingleBarcode".
    */
   static let readSingleBarcode = "ReadSingleBarcode"
   /**
    * This template is specially configured for recognizing numbers from the text lines. The template name is "RecognizeNumbers".
    */
   static let recognizeNumbers = "RecognizeNumbers"
   /**
    * This template is specially configured for recognizing letters from the text lines. The template name is "RecognizeLetters".
    */
   static let recognizeLetters = "RecognizeLetters"
   /**
    * This template is specially configured for recognizing number and letters from the text lines. The template name is "RecognizeNumbersAndLetters".
    */
   static let recognizeNumbersAndLetters = "RecognizeNumbersAndLetters"
   /**
    * This template is specially configured for recognizing number and upper case letters from the text lines. The template name is "RecognizeNumbersAndUppercaseLetters".
    */
   static let recognizeNumbersAndUppercaseLetters = "RecognizeNumbersAndUppercaseLetters"
   /**
    * This template is specially configured for recognizing upper case letters from the text lines. The template name is "RecognizeUppercaseLetters".
    */
   static let recognizeUppercaseLetters = "RecognizeUppercaseLetters"
}
```
