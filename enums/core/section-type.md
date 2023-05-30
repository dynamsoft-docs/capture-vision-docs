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
   >- C++
   >
>
```javascript
export enum EnumSectionType
{
   /**The result is output by "region prediction" section.*/
   ST_REGION_PREDETECTION = 0,
   /**The result is output by "barcode localization" section.*/
   ST_BARCODE_LOCALIZATION = 1,
   /**The result is output by "barcode decoding" section.*/
   ST_BARCODE_DECODING = 2,
   /**The result is output by "text line localization" section.*/
   ST_TEXT_LINE_LOCALIZATION = 3,
   /**The result is output by "text line  recognition" section.*/
   ST_TEXT_LINE_RECOGNITION = 4,
   /**The result is output by "document detection" section.*/
   ST_DOCUMENT_DETECTION = 5,
   /**The result is output by "document normalization" section.*/
   ST_DOCUMENT_NORMALIZATION = 6
}
```
>
```java
public class EnumSectionType
{
   /**The result is output by "region prediction" section.*/
   public static final int ST_REGION_PREDETECTION = 0;
   /**The result is output by "barcode localization" section.*/
   public static final int ST_BARCODE_LOCALIZATION = 1;
   /**The result is output by "barcode decoding" section.*/
   public static final int ST_BARCODE_DECODING = 2;
   /**The result is output by "text line localization" section.*/
   public static final int ST_TEXT_LINE_LOCALIZATION = 3;
   /**The result is output by "text line  recognition" section.*/
   public static final int ST_TEXT_LINE_RECOGNITION = 4;
   /**The result is output by "document detection" section.*/
   public static final int ST_DOCUMENT_DETECTION = 5;
   /**The result is output by "document normalization" section.*/
   public static final int ST_DOCUMENT_NORMALIZATION = 6;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSSectionType)
{
   /**The result is output by "region prediction" section.*/
   DSSectionTypeRegionPredection = 0,
   /**The result is output by "barcode localization" section.*/
   DSSectionTypeBarcodeLocalization = 1,
   /**The result is output by "barcode decoding" section.*/
   DSSectionTypeBarcodeDecoding = 2,
   /**The result is output by "text line localization" section.*/
   DSSectionTypeTextLineLocalization = 3,
   /**The result is output by "text line  recognition" section.*/
   DSSectionTypeTextLineRecognition = 4,
   /**The result is output by "document detection" section.*/
   DSSectionTypeDocumentDetection = 5,
   /**The result is output by "document normalization" section.*/
   DSSectionTypeDocumentNormalization = 6
}NS_SWIFT_NAME(SectionType);
```
>
```swift
public enum SectionType : Int
{
   /**The result is output by "region prediction" section.*/
   regionPredection = 0,
   /**The result is output by "barcode localization" section.*/
   barcodeLocalization = 1,
   /**The result is output by "barcode decoding" section.*/
   barcodeDecoding = 2,
   /**The result is output by "text line localization" section.*/
   textLineLocalization = 3,
   /**The result is output by "text line  recognition" section.*/
   textLineRecognition = 4,
   /**The result is output by "document detection" section.*/
   documentDetection = 5,
   /**The result is output by "document normalization" section.*/
   documentNormalization = 6
}
```
>
```cpp
typedef enum SectionType
{
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
