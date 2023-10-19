---
layout: default-layout
title: SectionType - Dynamsoft Core Enumerations
description: The enumeration SectionType of Dynamsoft Core describes the section of the algorithm.
keywords: Section type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: SectionType
codeAutoHeight: true
---

# Enumeration SectionType

`SectionType` describes the section of the algorithm. In the `IntermediateResultReceiver`, the `SectionType` indicate the algorithm section that produced the `IntermediateResult`.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumSectionType
{
   /**No section type is specified.*/
   ST_NULL = 0,
   /**The result is output by "region prediction" section.*/
   ST_REGION_PREDETECTION = 1,
   /**The result is output by "barcode localization" section.*/
   ST_BARCODE_LOCALIZATION = 2,
   /**The result is output by "barcode decoding" section.*/
   ST_BARCODE_DECODING = 3,
   /**The result is output by "text line localization" section.*/
   ST_TEXT_LINE_LOCALIZATION = 4,
   /**The result is output by "text line  recognition" section.*/
   ST_TEXT_LINE_RECOGNITION = 5,
   /**The result is output by "document detection" section.*/
   ST_DOCUMENT_DETECTION = 6,
   /**The result is output by "document normalization" section.*/
   ST_DOCUMENT_NORMALIZATION = 7
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumSectionType
{
   /**No section type is specified.*/
   public static final int ST_NULL = 0;
   /**The result is output by "region prediction" section.*/
   public static final int ST_REGION_PREDETECTION = 1;
   /**The result is output by "barcode localization" section.*/
   public static final int ST_BARCODE_LOCALIZATION = 2;
   /**The result is output by "barcode decoding" section.*/
   public static final int ST_BARCODE_DECODING = 3;
   /**The result is output by "text line localization" section.*/
   public static final int ST_TEXT_LINE_LOCALIZATION = 4;
   /**The result is output by "text line  recognition" section.*/
   public static final int ST_TEXT_LINE_RECOGNITION = 5;
   /**The result is output by "document detection" section.*/
   public static final int ST_DOCUMENT_DETECTION = 6;
   /**The result is output by "document normalization" section.*/
   public static final int ST_DOCUMENT_NORMALIZATION = 7;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSSectionType)
{
   /**No section type is specified.*/
   DSSectionTypeNull = 0,
   /**The result is output by "region prediction" section.*/
   DSSectionTypeRegionPredection = 1,
   /**The result is output by "barcode localization" section.*/
   DSSectionTypeBarcodeLocalization = 2,
   /**The result is output by "barcode decoding" section.*/
   DSSectionTypeBarcodeDecoding = 3,
   /**The result is output by "text line localization" section.*/
   DSSectionTypeTextLineLocalization = 4,
   /**The result is output by "text line  recognition" section.*/
   DSSectionTypeTextLineRecognition = 5,
   /**The result is output by "document detection" section.*/
   DSSectionTypeDocumentDetection = 6,
   /**The result is output by "document normalization" section.*/
   DSSectionTypeDocumentNormalization = 7
};
```
>
```swift
public enum SectionType : Int
{
   /**No section type is specified.*/
   null = 0,
   /**The result is output by "region prediction" section.*/
   regionPredection = 1,
   /**The result is output by "barcode localization" section.*/
   barcodeLocalization = 2,
   /**The result is output by "barcode decoding" section.*/
   barcodeDecoding = 3,
   /**The result is output by "text line localization" section.*/
   textLineLocalization = 4,
   /**The result is output by "text line  recognition" section.*/
   textLineRecognition = 5,
   /**The result is output by "document detection" section.*/
   documentDetection = 6,
   /**The result is output by "document normalization" section.*/
   documentNormalization = 7
}
```
>
```cpp
typedef enum SectionType
{
   /**No section type is specified.*/
   ST_NULL,
   /**The result is output by "region prediction" section.*/
   ST_REGION_PREDETECTION,
   /**The result is output by "barcode localization" section.*/
   ST_BARCODE_LOCALIZATION,
   /**The result is output by "barcode decoding" section.*/
   ST_BARCODE_DECODING,
   /**The result is output by "text line localization" section.*/
   ST_TEXT_LINE_LOCALIZATION,
   /**The result is output by "text line  recognition" section.*/
   ST_TEXT_LINE_RECOGNITION,
   /**The result is output by "document detection" section.*/
   ST_DOCUMENT_DETECTION,
   /**The result is output by "document normalization" section.*/
   ST_DOCUMENT_NORMALIZATION,
} SectionType;
```
