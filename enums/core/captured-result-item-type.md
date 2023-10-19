---
layout: default-layout
title: CapturedResultItemType - Dynamsoft Core Enumerations
description: The enumeration CapturedResultItemType of Dynamsoft Core describes all types of captured result item.
keywords: Captured result types
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CapturedResultItemType
codeAutoHeight: true
---

# Enumeration CapturedResultItemType

`CapturedResultItemType` describes all types of captured result item.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumCapturedResultItemType
{
   /** The type of the CapturedResultItem is "original image". */
   CRIT_ORIGINAL_IMAGE = 1,
   /** The type of the CapturedResultItem is "barcode". */
   CRIT_BARCODE = 2,
   /** The type of the CapturedResultItem is "text line". */
   CRIT_TEXT_LINE = 4,
   /** The type of the CapturedResultItem is "detected quad". */
   CRIT_DETECTED_QUAD = 8,
   /** The type of the CapturedResultItem is "normalized image". */
   CRIT_NORMALIZED_IMAGE = 16,
   /** The type of the CapturedResultItem is "parsed result". */
   CRIT_PARSE_RESULT = 32
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumCapturedResultItemType
{
   /** The type of the CapturedResultItem is "original image". */
   public static final int CRIT_ORIGINAL_IMAGE = 1;
   /** The type of the CapturedResultItem is "barcode". */
   public static final int CRIT_BARCODE = 2;
   /** The type of the CapturedResultItem is "text line". */
   public static final int CRIT_TEXT_LINE = 4;
   /** The type of the CapturedResultItem is "detected quad". */
   public static final int CRIT_DETECTED_QUAD = 8;
   /** The type of the CapturedResultItem is "normalized image". */
   public static final int CRIT_NORMALIZED_IMAGE = 16;
   /** The type of the CapturedResultItem is "parsed result". */
   public static final int CRIT_PARSED_RESULT = 32;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSCapturedResultItemType)
{
   /** The captured result is a original image. You can convert it into a DSOriginalImageResultItem. */
   DSCapturedResultItemTypeOriginalImage = 1,
   /** The captured result is a decoded barcode. You can convert it into a DSBarcodeResultItem. */
   DSCapturedResultItemTypeBarcode = 2,
   /** The captured result is a recognized text line. You can convert it into a DSTextLineResultItem. */
   DSCapturedResultItemTypeTextLine = 4,
   /** The captured result is a detected quadrilateral. You can convert it into a DSDetectedQuadResultItem. */
   DSCapturedResultItemTypeDetectedQuad = 8,
   /** The captured result is a normalized image. You can convert it into a DSNormalizedImageResultItem. */
   DSCapturedResultItemTypeNormalizedImage = 16,
   /** The captured result is a parsed result. You can convert it into a DSParsedResultItem. */
   DSCapturedResultItemTypeParsedResult = 32
};
```
>
```swift
public enum CapturedResultItemType : Int
{
   /** The captured result is a original image. You can convert it into a DSOriginalImageResultItem. */
   originalImage = 1
   /** The captured result is a decoded barcode. You can convert it into a DSBarcodeResultItem. */
   barcode = 2
   /** The captured result is a recognized text line. You can convert it into a DSTextLineResultItem. */
   textLine = 4
   /** The captured result is a detected quadrilateral. You can convert it into a DSDetectedQuadResultItem. */
   detectedQuad = 8
   /** The captured result is a normalized image. You can convert it into a DSNormalizedImageResultItem. */
   normalizedImage = 16
   /** The captured result is a parsed result. You can convert it into a DSParsedResultItem. */
   parsedResult = 32
};
```
>
```cpp
typedef enum CapturedResultItemType
{
   /** The type of the CapturedResultItem is "original image". */
   CRIT_ORIGINAL_IMAGE = 1,
   /** The type of the CapturedResultItem is "barcode". */
   CRIT_BARCODE = 2,
   /** The type of the CapturedResultItem is "text line". */
   CRIT_TEXT_LINE = 4,
   /** The type of the CapturedResultItem is "detected quad". */
   CRIT_DETECTED_QUAD = 8,
   /** The type of the CapturedResultItem is "normalized image". */
   CRIT_NORMALIZED_IMAGE = 16,
   /** The type of the CapturedResultItem is "parsed result". */
   CRIT_PARSED_RESULT = 32
} CapturedResultItemType;
```
