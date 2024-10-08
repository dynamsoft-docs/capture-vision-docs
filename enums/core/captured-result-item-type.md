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

`CapturedResultItemType` defines the various categories of items that can be recognized and captured.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >- C#
   >- Python
   >
>
```javascript
enum EnumCapturedResultItemType {
    /**
     * Represents an original image captured by the system.
     * This type is used to identify the raw, unmodified image data directly obtained from the image source.
     */
    CRIT_ORIGINAL_IMAGE = 1,
    /**
     * Identifies a captured item as a barcode within the image.
     * This type signifies that the item has been recognized as a barcode and contains data extracted from the barcode.
     */
    CRIT_BARCODE = 2,
    /**
     * Identifies a captured item as a line of text within the image.
     * This type signifies that the item has been recognized as a line of text and contains the textual content.
     */
    CRIT_TEXT_LINE = 4,
    /**
     * Identifies a captured item as a quadrilateral detected within the image.
     * This type is typically used for geometric shapes or areas of interest that have been identified, often in the context of document scanning.
     */
    CRIT_DETECTED_QUAD = 8,
    /**
     * Represents an image that has been processed and normalized based on the original image.
     * Normalization may include adjustments such as deskewing, perspective correction, etc. to standardize the image presentation.
     */
    CRIT_NORMALIZED_IMAGE = 16,
    /**
     * Indicates a parsed result item.
     * This type is used for items that have undergone further interpretation by Dynamsoft Code Parser, transforming raw data into a structured format.
     */
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
>
```csharp
public enum EnumCapturedResultItemType
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
}
```
>
```python
class EnumCapturedResultItemType(IntEnum):
    # The type of the CapturedResultItem is "original image".
    CRIT_ORIGINAL_IMAGE = 1
    # The type of the CapturedResultItem is "barcode".
    CRIT_BARCODE = 2
    # The type of the CapturedResultItem is "text line".
    CRIT_TEXT_LINE = 4
    # The type of the CapturedResultItem is "detected quad".
    CRIT_DETECTED_QUAD = 8
    # The type of the CapturedResultItem is "normalized image".
    CRIT_NORMALIZED_IMAGE = 16
    # The type of the CapturedResultItem is "parsed result".
    CRIT_PARSED_RESULT = 32
```
