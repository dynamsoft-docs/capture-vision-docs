---
layout: default-layout
title: IntermediateResultUnitType - Dynamsoft Core Enumerations
description: The enumeration IntermediateResultUnitType of Dynamsoft Core describes the type of the intermediate result unit.
keywords: Intermediate result unit type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: IntermediateResultUnitType
codeAutoHeight: true
---

# Enumeration IntermediateResultUnitType

`IntermediateResultUnitType` defines different types of intermediate results generated or expected to be generated during image processing.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumIntermediateResultUnitType {
    /** No intermediate result. */
    IRUT_NULL = 0,
    /** A full-color image. */
    IRUT_COLOUR_IMAGE = 1,
    /** A color image that has been scaled down for efficiency. */
    IRUT_SCALED_DOWN_COLOUR_IMAGE = 1 << 1,
    /** A grayscale image derived from the original input. */
    IRUT_GRAYSCALE_IMAGE = 1 << 2,
    /** A grayscale image that has undergone transformation. */
    IRUT_TRANSOFORMED_GRAYSCALE_IMAGE = 1 << 3,
    /** A grayscale image enhanced for further processing. */
    IRUT_ENHANCED_GRAYSCALE_IMAGE = 1 << 4,
    /** Regions pre-detected as potentially relevant for further analysis. */
    IRUT_PREDETECTED_REGIONS = 1 << 5,
    /** A binary (black and white) image. */
    IRUT_BINARY_IMAGE = 1 << 6,
    /** Results from detecting textures within the image. */
    IRUT_TEXTURE_DETECTION_RESULT = 1 << 7,
    /** A grayscale image with textures removed to enhance subject details like text or barcodes. */
    IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE = 1 << 8,
    /** A binary image with textures removed, useful for clear detection of subjects without background noise. */
    IRUT_TEXTURE_REMOVED_BINARY_IMAGE = 1 << 9,
    /** Detected contours within the image, which can help in identifying shapes and objects. */
    IRUT_CONTOURS = 1 << 10,
    /** Detected line segments, useful in structural analysis of the image content. */
    IRUT_LINE_SEGMENTS = 1 << 11,
    /** Identified text zones, indicating areas with potential textual content. */
    IRUT_TEXT_ZONES = 1 << 12,
    /** A binary image with text regions removed. */
    IRUT_TEXT_REMOVED_BINARY_IMAGE = 1 << 13,
    /** Zones identified as potential barcode areas, aiding in focused barcode detection. */
    IRUT_CANDIDATE_BARCODE_ZONES = 1 << 14,
    /** Barcodes that have been localized but not yet decoded. */
    IRUT_LOCALIZED_BARCODES = 1 << 15,
    /** Barcode images scaled up for improved readability or decoding accuracy. */
    IRUT_SCALED_UP_BARCODE_IMAGE = 1 << 16,
    /** Images of barcodes processed to resist deformation and improve decoding success. */
    IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE = 1 << 17,
    /** Barcode images that have been complemented. */
    IRUT_COMPLEMENTED_BARCODE_IMAGE = 1 << 18,
    /** Successfully decoded barcodes. */
    IRUT_DECODED_BARCODES = 1 << 19,
    /** Detected long lines. */
    IRUT_LONG_LINES = 1 << 20,
    /** Detected corners within the image. */
    IRUT_CORNERS = 1 << 21,
    /** Candidate edges identified as potential components of quadrilaterals. */
    IRUT_CANDIDATE_QUAD_EDGES = 1 << 22,
    /** Successfully detected quadrilaterals. */
    IRUT_DETECTED_QUADS = 1 << 23,
    /** Text lines that have been localized in preparation for recognition. */
    IRUT_LOCALIZED_TEXT_LINES = 1 << 24,
    /** Successfully recognized text lines. */
    IRUT_RECOGNIZED_TEXT_LINES = 1 << 25,
    /** Successfully normalized images. */
    IRUT_NORMALIZED_IMAGES = 1 << 26,
    /** A mask to select all types of intermediate results. */
    IRUT_ALL = 0xFFFFFFF
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumIntermediateResultUnitType
{
   /**No IntermediateResult type is specified.*/
   public static final long IRUT_NULL = 0
   /**The type of the IntermediateResult is "colour image".*/
   public static final long IRUT_COLOUR_IMAGE = 1
   /**The type of the IntermediateResult is "scaled down colour image".*/
   public static final long IRUT_SCALED_DOWN_COLOUR_IMAGE = 2
   /**The type of the IntermediateResult is "grayscale image".*/
   public static final long IRUT_GRAYSCALE_IMAGE = 3
   /**The type of the IntermediateResult is "transformed grayscale image".*/
   public static final long IRUT_TRANSFORMED_GRAYSCALE_IMAGE = 4
   /**The type of the IntermediateResult is "enhanced grayscale image".*/
   public static final long IRUT_ENHANCED_GRAYSCALE_IMAGE = 5
   /**The type of the IntermediateResult is "predected regions".*/
   public static final long IRUT_PREDETECTED_REGIONS = 6
   /**The type of the IntermediateResult is "binary image".*/
   public static final long IRUT_BINARY_IMAGE = 7
   /**The type of the IntermediateResult is "texture detection result".*/
   public static final long IRUT_TEXTURE_DETECTION_RESULT = 8
   /**The type of the IntermediateResult is "texture removed grayscale image".*/
   public static final long IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE = 9
   /**The type of the IntermediateResult is "texture removed binary image".*/
   public static final long IRUT_TEXTURE_REMOVED_BINARY_IMAGE = 10
   /**The type of the IntermediateResult is "contours".*/
   public static final long IRUT_CONTOURS = 11
   /**The type of the IntermediateResult is "line segments".*/
   public static final long IRUT_LINE_SEGMENTS = 12
   /**The type of the IntermediateResult is "text zones".*/
   public static final long IRUT_TEXT_ZONES = 13
   /**The type of the IntermediateResult is "text removed binary image".*/
   public static final long IRUT_TEXT_REMOVED_BINARY_IMAGE = 14
   /**The type of the IntermediateResult is "candidate barcode zones".*/
   public static final long IRUT_CANDIDATE_BARCODE_ZONES = 15
   /**The type of the IntermediateResult is "localized barcodes".*/
   public static final long IRUT_LOCALIZED_BARCODES = 16
   /**The type of the IntermediateResult is "scaled up barcode image".*/
   public static final long IRUT_SCALED_UP_BARCODE_IMAGE = 17
   /**The type of the IntermediateResult is "deformation resisted barcode image".*/
   public static final long IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE = 18
   /**The type of the IntermediateResult is "complemented barcode image".*/
   public static final long IRUT_COMPLEMENTED_BARCODE_IMAGE = 19
   /**The type of the IntermediateResult is "decoded barcodes".*/
   public static final long IRUT_DECODED_BARCODES = 20
   /**The type of the IntermediateResult is "long lines".*/
   public static final long IRUT_LONG_LINES = 21
   /**The type of the IntermediateResult is "corners".*/
   public static final long IRUT_CORNERS = 22
   /**The type of the IntermediateResult is "candidate quad edges".*/
   public static final long IRUT_CANDIDATE_QUAD_EDGES = 23
   /**The type of the IntermediateResult is "detected quads".*/
   public static final long IRUT_DETECTED_QUADS = 24
   /**The type of the IntermediateResult is "localized text lines".*/
   public static final long IRUT_LOCALIZED_TEXT_LINES = 25
   /**The type of the IntermediateResult is "recognized text lines".*/
   public static final long IRUT_RECOGNIZED_TEXT_LINES = 26
   /**The type of the IntermediateResult is "normalized image".*/
   public static final long IRUT_NORMALIZED_IMAGES = 27
   /**The type of the IntermediateResult is "all".*/
   public static final long IRUT_ALL = 0x7FFFFFF
}
```
>
```objc
typedef NS_OPTIONS(NSUInteger, DSIntermediateResultUnitType)
{
   /**No IntermediateResult type is specified.*/
   DSIntermediateResultUnitTypeNull = 0,
   /**The type of the IntermediateResult is "colour image".*/
   DSIntermediateResultUnitTypeColourImage = 1,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeScaledDownColourImage = 1 << 1,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeGrayscaleImage = 1 << 2,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeTransformedGrayscaleImage = 1 << 3,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeEnhancedGrayscaleImage = 1 << 4,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypePredetectedRegions = 1 << 5,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeBinaryImage = 1 << 6,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeTextureDetectionResult = 1 << 7,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeTextureRemovedGrayscaleImage = 1 << 8,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeTextureRemovedBinaryImage = 1 << 9,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeContours = 1 << 10,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeLineSegments = 1 << 11,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeTextZones = 1 << 12,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeTextRemovedBinaryImage = 1 << 13,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeCandidateBarcodeZones = 1 << 14,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeLocalizedBarcodes = 1 << 15,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeScaledUpBarcodeImage = 1 << 16,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeDeformationResistedBarcodeImage = 1 << 17,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeComplementedBarcodeImage = 1 << 18,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeDecodedBarcode = 1 << 19,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeLongLines = 1 << 20,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeCorners = 1 << 21,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeCandidateQuadEdges = 1 << 22,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeDetectedQuads = 1 << 23,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeLocalizedTextLines = 1 << 24,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeRecognizedTextLine = 1 << 25,
   /**The type of the IntermediateResult is "".*/
   DSIntermediateResultUnitTypeNormalizedImages = 1 << 26,
   /**Specify all intermediate result types.*/
   DSIntermediateResultUnitTypeAll = 0x3FFFFFF
};
```
>
```swift
public enum IntermediateResultUnitType : Int
{
   /**No IntermediateResult type is specified.*/
   null = 0,
   /**The type of the IntermediateResult is "colour image".*/
   colourImage = 1,
   /**The type of the IntermediateResult is "scaled down colour image".*/
   scaledDownColourImage = 1 << 1,
   /**The type of the IntermediateResult is "grayscale image".*/
   grayscaleImage = 1 << 2,
   /**The type of the IntermediateResult is "transformed grayscale image".*/
   transformedGrayscaleImage = 1 << 3,
   /**The type of the IntermediateResult is "enhanced grayscale image".*/
   enhancedGrayscaleImage = 1 << 4,
   /**The type of the IntermediateResult is "predected regions".*/
   predetectedRegions = 1 << 5,
   /**The type of the IntermediateResult is "binary image".*/
   binaryImage = 1 << 6,
   /**The type of the IntermediateResult is "texture detection result".*/
   textureDetectionResult = 1 << 7,
   /**The type of the IntermediateResult is "texture removed grayscale image".*/
   textureRemovedGrayscaleImage = 1 << 8,
   /**The type of the IntermediateResult is "texture removed binary image".*/
   textureRemovedBinaryImage = 1 << 9,
   /**The type of the IntermediateResult is "contours".*/
   contours = 1 << 10,
   /**The type of the IntermediateResult is "line segments".*/
   lineSegments = 1 << 11,
   /**The type of the IntermediateResult is "text zones".*/
   textZones = 1 << 12,
   /**The type of the IntermediateResult is "text removed binary image".*/
   textRemovedBinaryImage = 1 << 13,
   /**The type of the IntermediateResult is "candidate barcode zones".*/
   candidateBarcodeZones = 1 << 14,
   /**The type of the IntermediateResult is "localized barcodes".*/
   localizedBarcodes = 1 << 15,
   /**The type of the IntermediateResult is "scaled up barcode image".*/
   scaledUpBarcodeImage = 1 << 16,
   /**The type of the IntermediateResult is "deformation resisted barcode image".*/
   deformationResistedBarcodeImage = 1 << 17,
   /**The type of the IntermediateResult is "complemented barcode image".*/
   complementedBarcodeImage = 1 << 18,
   /**The type of the IntermediateResult is "decoded barcodes".*/
   decodedBarcode = 1 << 19,
   /**The type of the IntermediateResult is "long lines".*/
   longLines = 1 << 20,
   /**The type of the IntermediateResult is "corners".*/
   corners = 1 << 21,
   /**The type of the IntermediateResult is "candidate quad edges".*/
   candidateQuadEdges = 1 << 22,
   /**The type of the IntermediateResult is "detected quads".*/
   detectedQuads = 1 << 23,
   /**The type of the IntermediateResult is "localized text lines".*/
   localizedTextLines = 1 << 24,
   /**The type of the IntermediateResult is "recognized text lines".*/
   recognizedTextLine = 1 << 25,
   /**The type of the IntermediateResult is "normalized image".*/
   normalizedImages = 1 << 26,
   /**Specify all intermediate result types.*/
   all = 0x3FFFFFF
}
```
>
```cpp
enum IntermediateResultUnitType : unsigned long long
{
   /**No IntermediateResult type is specified.*/
   IRUT_NULL = 0,
   /**The type of the IntermediateResult is "colour image".*/
   IRUT_COLOUR_IMAGE = 1,
   /**The type of the IntermediateResult is "scaled down colour image".*/
   IRUT_SCALED_DOWN_COLOUR_IMAGE = 1 << 1,
   /**The type of the IntermediateResult is "grayscale image".*/
   IRUT_GRAYSCALE_IMAGE = 1 << 2,
   /**The type of the IntermediateResult is "transformed grayscale image".*/
   IRUT_TRANSFORMED_GRAYSCALE_IMAGE = 1 << 3,
   /**The type of the IntermediateResult is "enhanced grayscale image".*/
   IRUT_ENHANCED_GRAYSCALE_IMAGE = 1 << 4,
   /**The type of the IntermediateResult is "predected regions".*/
   IRUT_PREDETECTED_REGIONS = 1 << 5,
   /**The type of the IntermediateResult is "binary image".*/
   IRUT_BINARY_IMAGE = 1 << 6,
   /**The type of the IntermediateResult is "texture detection result".*/
   IRUT_TEXTURE_DETECTION_RESULT = 1 << 7,
   /**The type of the IntermediateResult is "texture removed grayscale image".*/
   IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE = 1 << 8,
   /**The type of the IntermediateResult is "texture removed binary image".*/
   IRUT_TEXTURE_REMOVED_BINARY_IMAGE = 1 << 9,
   /**The type of the IntermediateResult is "contours".*/
   IRUT_CONTOURS = 1 << 10,
   /**The type of the IntermediateResult is "line segments".*/
   IRUT_LINE_SEGMENTS = 1 << 11,
   /**The type of the IntermediateResult is "text zones".*/
   IRUT_TEXT_ZONES = 1 << 12,
   /**The type of the IntermediateResult is "text removed binary image".*/
   IRUT_TEXT_REMOVED_BINARY_IMAGE = 1 << 13,
   /**The type of the IntermediateResult is "candidate barcode zones".*/
   IRUT_CANDIDATE_BARCODE_ZONES = 1 << 14,
   /**The type of the IntermediateResult is "localized barcodes".*/
   IRUT_LOCALIZED_BARCODES = 1 << 15,
   /**The type of the IntermediateResult is "scaled up barcode image".*/
   IRUT_SCALED_UP_BARCODE_IMAGE = 1 << 16,
   /**The type of the IntermediateResult is "deformation resisted barcode image".*/
   IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE = 1 << 17,
   /**The type of the IntermediateResult is "complemented barcode image".*/
   IRUT_COMPLEMENTED_BARCODE_IMAGE = 1 << 18,
   /**The type of the IntermediateResult is "decoded barcodes".*/
   IRUT_DECODED_BARCODES = 1 << 19,
   /**The type of the IntermediateResult is "long lines".*/
   IRUT_LONG_LINES = 1 << 20,
   /**The type of the IntermediateResult is "corners".*/
   IRUT_CORNERS = 1 << 21,
   /**The type of the IntermediateResult is "candidate quad edges".*/
   IRUT_CANDIDATE_QUAD_EDGES = 1 << 22,
   /**The type of the IntermediateResult is "detected quads".*/
   IRUT_DETECTED_QUADS = 1 << 23,
   /**The type of the IntermediateResult is "localized text lines".*/
   IRUT_LOCALIZED_TEXT_LINES = 1 << 24,
   /**The type of the IntermediateResult is "recognized text lines".*/
   IRUT_RECOGNIZED_TEXT_LINES = 1 << 25,
   /**The type of the IntermediateResult is "normalized image".*/
   IRUT_NORMALIZED_IMAGES = 1 << 26,
   /**The type of the IntermediateResult is "all".*/
   IRUT_ALL = 0x7FFFFFF
};
```
