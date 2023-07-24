---
layout: default-layout
Title: RegionObjectElementType - Dynamsoft Core Enumerations
Description: The enumeration RegionObjectElementType of Dynamsoft Core describes the types of RegionObjectElement.
Keywords: Region object element type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RegionObjectElementType
codeAutoHeight: true
---

# Enumeration RegionObjectElementType

`RegionObjectElementType` is used to determine the particular type of the subclasses of `RegionObjectElement`.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
export enum EnumRegionObjectElementType {
   /**The type of subclass PredetectedRegionElement.*/
   ROET_PREDETECTED_REGION = 0,
   /**The type of subclass LocalizedBarcodeElement.*/
   ROET_LOCALIZED_BARCODE = 1,
   /**The type of subclass DecodedBarcodeElement.*/
   ROET_DECODED_BARCODE = 2,
   /**The type of subclass LocalizedTextLineElement.*/
   ROET_LOCALIZED_TEXT_LINE = 3,
   /**The type of subclass RecognizedTextLineElement.*/
   ROET_RECOGNIZED_TEXT_LINE = 4,
   /**The type of subclass DetectedQuadElement.*/
   ROET_DETECTED_QUAD = 5,
   /**The type of subclass NormalizedImageElement.*/
   ROET_NORMALIZED_IMAGE = 6
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumRegionObjectElementType
{
   /**The type of subclass PredetectedRegionElement.*/
   public static final int ROET_PREDETECTED_REGION = 0;
   /**The type of subclass LocalizedBarcodeElement.*/
   public static final int ROET_LOCALIZED_BARCODE = 1;
   /**The type of subclass DecodedBarcodeElement.*/
   public static final int ROET_DECODED_BARCODE = 2;
   /**The type of subclass LocalizedTextLineElement.*/
   public static final int ROET_LOCALIZED_TEXT_LINE = 3;
   /**The type of subclass RecognizedTextLineElement.*/
   public static final int ROET_RECOGNIZED_TEXT_LINE = 4;
   /**The type of subclass DetectedQuadElement.*/
   public static final int ROET_DETECTED_QUAD = 5;
   /**The type of subclass NormalizedImageElement.*/
   public static final int ROET_NORMALIZED_IMAGE = 6;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSRegionObjectElementType)
{
   /**The type of subclass PredetectedRegionElement.*/
   DSRegionObjectElementTypePredetectedRegion = 0,
   /**The type of subclass LocalizedBarcodeElement.*/
   DSRegionObjectElementTypeLocalizedBarcode = 1,
   /**The type of subclass DecodedBarcodeElement.*/
   DSRegionObjectElementTypeDecodedBarcode = 2,
   /**The type of subclass LocalizedTextLineElement.*/
   DSRegionObjectElementTypeLocalizedTextLine = 3,
   /**The type of subclass RecognizedTextLineElement.*/
   DSRegionObjectElementTypeRecognizedTextLine = 4,
   /**The type of subclass DetectedQuadElement.*/
   DSRegionObjectElementTypeDetectedQuad = 5,
   /**The type of subclass NormalizedImageElement.*/
   DSRegionObjectElementTypeNormalizedImage = 6
};
```
>
```swift
public enum RegionObjectElementType : Int
{
   /**The type of subclass PredetectedRegionElement.*/
   predetectedRegion = 0,
   /**The type of subclass LocalizedBarcodeElement.*/
   localizedBarcode = 1,
   /**The type of subclass DecodedBarcodeElement.*/
   decodedBarcode = 2,
   /**The type of subclass LocalizedTextLineElement.*/
   localizedTextLine = 3,
   /**The type of subclass RecognizedTextLineElement.*/
   recognizedTextLine = 4,
   /**The type of subclass DetectedQuadElement.*/
   detectedQuad = 5,
   /**The type of subclass NormalizedImageElement.*/
   normalizedImage = 6
}
```
>
```cpp
typedef enum RegionObjectElementType
{
   /**The type of subclass PredetectedRegionElement.*/
   ROET_PREDETECTED_REGION,
   /**The type of subclass LocalizedBarcodeElement.*/
   ROET_LOCALIZED_BARCODE,
   /**The type of subclass DecodedBarcodeElement.*/
   ROET_DECODED_BARCODE,
   /**The type of subclass LocalizedTextLineElement.*/
   ROET_LOCALIZED_TEXT_LINE,
   /**The type of subclass RecognizedTextLineElement.*/
   ROET_RECOGNIZED_TEXT_LINE,
   /**The type of subclass DetectedQuadElement.*/
   ROET_DETECTED_QUAD,
   /**The type of subclass NormalizedImageElement.*/
   ROET_NORMALIZED_IMAGE,
   /**The type of subclass SourceImageElement.*/
   ROET_SOURCE_IMAGE,
   /**The type of subclass TargetROIElement.*/
   ROET_TARGET_ROI
} RegionObjectElementType;
```
