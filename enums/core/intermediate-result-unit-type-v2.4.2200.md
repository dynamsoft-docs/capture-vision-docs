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
    /**Detected short lines.*/
    IRUT_SHORT_LINES = 1 << 27,
    /**grouped lines of text.*/
    IRUT_TEXT_LINE_GROUPS = 1 << 28,
    /** A mask to select all types of intermediate results. */
    IRUT_ALL = 0xFFFFFFFFFFFFFFFF
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumIntermediateResultUnitType {
    /** No intermediate result. */
    long IRUT_NULL = 0L;
    /** A full-color image. */
    long IRUT_COLOUR_IMAGE = 1L;
    /** A color image that has been scaled down for efficiency. */
    long IRUT_SCALED_DOWN_COLOUR_IMAGE = 1L << 1;
    /** A grayscale image derived from the original input. */
    long IRUT_GRAYSCALE_IMAGE = 1L << 2;
    /** A grayscale image that has undergone transformation. */
    long IRUT_TRANSOFORMED_GRAYSCALE_IMAGE = 1L << 3;
    /** A grayscale image enhanced for further processing. */
    long IRUT_ENHANCED_GRAYSCALE_IMAGE = 1L << 4;
    /** Regions pre-detected as potentially relevant for further analysis. */
    long IRUT_PREDETECTED_REGIONS = 1L << 5;
    /** A binary (black and white) image. */
    long IRUT_BINARY_IMAGE = 1L << 6;
    /** Results from detecting textures within the image. */
    long IRUT_TEXTURE_DETECTION_RESULT = 1L << 7;
    /** A grayscale image with textures removed to enhance subject details like text or barcodes. */
    long IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE = 1L << 8;
    /** A binary image with textures removed, useful for clear detection of subjects without background noise. */
    long IRUT_TEXTURE_REMOVED_BINARY_IMAGE = 1L << 9;
    /** Detected contours within the image, which can help in identifying shapes and objects. */
    long IRUT_CONTOURS = 1L << 10;
    /** Detected line segments, useful in structural analysis of the image content. */
    long IRUT_LINE_SEGMENTS = 1L << 11;
    /** Identified text zones, indicating areas with potential textual content. */
    long IRUT_TEXT_ZONES = 1L << 12;
    /** A binary image with text regions removed. */
    long IRUT_TEXT_REMOVED_BINARY_IMAGE = 1L << 13;
    /** Zones identified as potential barcode areas, aiding in focused barcode detection. */
    long IRUT_CANDIDATE_BARCODE_ZONES = 1L << 14;
    /** Barcodes that have been localized but not yet decoded. */
    long IRUT_LOCALIZED_BARCODES = 1L << 15;
    /** Barcode images scaled up for improved readability or decoding accuracy. */
    long IRUT_SCALED_UP_BARCODE_IMAGE = 1L << 16;
    /** Images of barcodes processed to resist deformation and improve decoding success. */
    long IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE = 1L << 17;
    /** Barcode images that have been complemented. */
    long IRUT_COMPLEMENTED_BARCODE_IMAGE = 1L << 18;
    /** Successfully decoded barcodes. */
    long IRUT_DECODED_BARCODES = 1L << 19;
    /** Detected long lines. */
    long IRUT_LONG_LINES = 1L << 20;
    /** Detected corners within the image. */
    long IRUT_CORNERS = 1L << 21;
    /** Candidate edges identified as potential components of quadrilaterals. */
    long IRUT_CANDIDATE_QUAD_EDGES = 1L << 22;
    /** Successfully detected quadrilaterals. */
    long IRUT_DETECTED_QUADS = 1L << 23;
    /** Text lines that have been localized in preparation for recognition. */
    long IRUT_LOCALIZED_TEXT_LINES = 1L << 24;
    /** Successfully recognized text lines. */
    long IRUT_RECOGNIZED_TEXT_LINES = 1L << 25;
    /** Successfully normalized images. */
    long IRUT_NORMALIZED_IMAGES = 1L << 26;
    /** Detected short lines. */
    long IRUT_SHORT_LINES = 1L << 27;
    /** Recognized raw text lines. */
    public static final long IRUT_RAW_TEXT_LINES = 1 << 28;
    /** A mask to select all types of intermediate results. */
    long IRUT_ALL = 0xFFFFFFFFFFFFFFFF;
}
```
>
```objc
typedef NS_OPTIONS(NSUInteger, DSIntermediateResultUnitType) {
    /** No intermediate result. */
    DSIntermediateResultUnitTypeNull = 0,
    /** A full-color image. */
    DSIntermediateResultUnitTypeColourImage = 1,
    /** A color image that has been scaled down for efficiency. */
    DSIntermediateResultUnitTypeScaledDownColourImage = 1 << 1,
    /** A grayscale image derived from the original input. */
    DSIntermediateResultUnitTypeGrayscaleImage = 1 << 2,
    /** A grayscale image that has undergone transformation. */
    DSIntermediateResultUnitTypeTransformedGrayscaleImage = 1 << 3,
    /** A grayscale image enhanced for further processing. */
    DSIntermediateResultUnitTypeEnhancedGrayscaleImage = 1 << 4,
    /** Regions pre-detected as potentially relevant for further analysis. */
    DSIntermediateResultUnitTypePredetectedRegions = 1 << 5,
    /** A binary (black and white) image. */
    DSIntermediateResultUnitTypeBinaryImage = 1 << 6,
    /** Results from detecting textures within the image. */
    DSIntermediateResultUnitTypeTextureDetectionResult = 1 << 7,
    /** A grayscale image with textures removed to enhance subject details like text or barcodes. */
    DSIntermediateResultUnitTypeTextureRemovedGrayscaleImage = 1 << 8,
    /** A binary image with textures removed, useful for clear detection of subjects without background noise. */
    DSIntermediateResultUnitTypeTextureRemovedBinaryImage = 1 << 9,
    /** Detected contours within the image, which can help in identifying shapes and objects. */
    DSIntermediateResultUnitTypeContours = 1 << 10,
    /** Detected line segments, useful in structural analysis of the image content. */
    DSIntermediateResultUnitTypeLineSegments = 1 << 11,
    /** Identified text zones, indicating areas with potential textual content. */
    DSIntermediateResultUnitTypeTextZones = 1 << 12,
    /** A binary image with text regions removed. */
    DSIntermediateResultUnitTypeTextRemovedBinaryImage = 1 << 13,
    /** Zones identified as potential barcode areas, aiding in focused barcode detection. */
    DSIntermediateResultUnitTypeCandidateBarcodeZones = 1 << 14,
    /** Barcodes that have been localized but not yet decoded. */
    DSIntermediateResultUnitTypeLocalizedBarcodes = 1 << 15,
    /** Barcode images scaled up for improved readability or decoding accuracy. */
    DSIntermediateResultUnitTypeScaledUpBarcodeImage = 1 << 16,
    /** Images of barcodes processed to resist deformation and improve decoding success. */
    DSIntermediateResultUnitTypeDeformationResistedBarcodeImage = 1 << 17,
    /** Barcode images that have been complemented. */
    DSIntermediateResultUnitTypeComplementedBarcodeImage = 1 << 18,
    /** Successfully decoded barcodes. */
    DSIntermediateResultUnitTypeDecodedBarcodes = 1 << 19,
    /** Detected long lines. */
    DSIntermediateResultUnitTypeLongLines = 1 << 20,
    /** Detected corners within the image. */
    DSIntermediateResultUnitTypeCorners = 1 << 21,
    /** Candidate edges identified as potential components of quadrilaterals. */
    DSIntermediateResultUnitTypeCandidateQuadEdges = 1 << 22,
    /** Successfully detected quadrilaterals. */
    DSIntermediateResultUnitTypeDetectedQuads = 1 << 23,
    /** Text lines that have been localized in preparation for recognition. */
    DSIntermediateResultUnitTypeLocalizedTextLines = 1 << 24,
    /** Successfully recognized text lines. */
    DSIntermediateResultUnitTypeRecognizedTextLines = 1 << 25,
    /** Successfully normalized images. */
    DSIntermediateResultUnitTypeNormalizedImages = 1 << 26,
    /** Detected short lines. */
    DSIntermediateResultUnitTypeShortLines = 1 << 27,
    /** Recognized raw text lines. */
    DSIntermediateResultUnitTypeRawTextLines = 1 << 28,
    /** A mask to select all types of intermediate results. */
    DSIntermediateResultUnitTypeAll = 0xFFFFFFFFFFFFFFFF
};
```
>
```swift
public enum IntermediateResultUnitType: Int {
    /** No intermediate result. */
    case null = 0
    /** A full-color image. */
    case colourImage = 1
    /** A color image that has been scaled down for efficiency. */
    case scaledDownColourImage = 1 << 1
    /** A grayscale image derived from the original input. */
    case grayscaleImage = 1 << 2
    /** A grayscale image that has undergone transformation. */
    case transformedGrayscaleImage = 1 << 3
    /** A grayscale image enhanced for further processing. */
    case enhancedGrayscaleImage = 1 << 4
    /** Regions pre-detected as potentially relevant for further analysis. */
    case predetectedRegions = 1 << 5
    /** A binary (black and white) image. */
    case binaryImage = 1 << 6
    /** Results from detecting textures within the image. */
    case textureDetectionResult = 1 << 7
    /** A grayscale image with textures removed to enhance subject details like text or barcodes. */
    case textureRemovedGrayscaleImage = 1 << 8
    /** A binary image with textures removed, useful for clear detection of subjects without background noise. */
    case textureRemovedBinaryImage = 1 << 9
    /** Detected contours within the image, which can help in identifying shapes and objects. */
    case contours = 1 << 10
    /** Detected line segments, useful in structural analysis of the image content. */
    case lineSegments = 1 << 11
    /** Identified text zones, indicating areas with potential textual content. */
    case textZones = 1 << 12
    /** A binary image with text regions removed. */
    case textRemovedBinaryImage = 1 << 13
    /** Zones identified as potential barcode areas, aiding in focused barcode detection. */
    case candidateBarcodeZones = 1 << 14
    /** Barcodes that have been localized but not yet decoded. */
    case localizedBarcodes = 1 << 15
    /** Barcode images scaled up for improved readability or decoding accuracy. */
    case scaledUpBarcodeImage = 1 << 16
    /** Images of barcodes processed to resist deformation and improve decoding success. */
    case deformationResistedBarcodeImage = 1 << 17
    /** Barcode images that have been complemented. */
    case complementedBarcodeImage = 1 << 18
    /** Successfully decoded barcodes. */
    case decodedBarcodes = 1 << 19
    /** Detected long lines. */
    case longLines = 1 << 20
    /** Detected corners within the image. */
    case corners = 1 << 21
    /** Candidate edges identified as potential components of quadrilaterals. */
    case candidateQuadEdges = 1 << 22
    /** Successfully detected quadrilaterals. */
    case detectedQuads = 1 << 23
    /** Text lines that have been localized in preparation for recognition. */
    case localizedTextLines = 1 << 24
    /** Successfully recognized text lines. */
    case recognizedTextLines = 1 << 25
    /** Successfully normalized images. */
    case normalizedImages = 1 << 26
    /** Detected short lines. */
    case shortLines = 1 << 27
    /** Recognized raw text lines. */
    rawTextLines = 1 << 28
    /** A mask to select all types of intermediate results. */
    case all = 0xFFFFFFFFFFFFFFFF
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
	/**The type of the IntermediateResult is "short lines".*/
	IRUT_SHORT_LINES = 1 << 27,
	/**The type of the IntermediateResult is "text line groups".*/
	IRUT_RAW_TEXT_LINES = 1LL << 28,
	/**The type of the IntermediateResult is "all".*/
	IRUT_ALL = 0xFFFFFFFFFFFFFFFF
};
```
