---
layout: default-layout
Title: IntermediateResultUnitType - Dynamsoft Core Enumerations
Description: The enumeration IntermediateResultUnitType of Dynamsoft Core describes the type of the intermediate result unit.
Keywords: Intermediate result unit type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: IntermediateResultUnitType
---

# Enumeration IntermediateResultUnitType

Describes the type of the intermediate result unit. Enumeration `IntermediateResultUnitType` is used in each subclass of `IntermediateResult` to indicate the type of the result. It is also used to declare which kinds `IntermediateResult` should be output by the library.

```cpp
enum IntermediateResultUnitType : unsigned long long
{
    /** No IntermediateResult type is specified. */
    IRUT_NULL = 0,
    /** The type of the IntermediateResult is "colour image". */
    IRUT_COLOUR_IMAGE = 1,
    /** The type of the IntermediateResult is "scaled down colour image". */
    IRUT_SCALED_DOWN_COLOUR_IMAGE = 1 << 1,
    /** The type of the IntermediateResult is "grayscale image". */
    IRUT_GRAYSCALE_IMAGE = 1 << 2,
    /** The type of the IntermediateResult is "transformed grayscale image". */
    IRUT_TRANSFORMED_GRAYSCALE_IMAGE = 1 << 3,
    /** The type of the IntermediateResult is "enhanced grayscale image". */
    IRUT_ENHANCED_GRAYSCALE_IMAGE = 1 << 4,
    /** The type of the IntermediateResult is "predected regions". */
    IRUT_PREDETECTED_REGIONS = 1 << 5,
    /** The type of the IntermediateResult is "binary image". */
    IRUT_BINARY_IMAGE = 1 << 6,
    /** The type of the IntermediateResult is "texture detection result". */
    IRUT_TEXTURE_DETECTION_RESULT = 1 << 7,
    /** The type of the IntermediateResult is "texture removed grayscale image". */
    IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE = 1 << 8,
    /** The type of the IntermediateResult is "texture removed binary image". */
    IRUT_TEXTURE_REMOVED_BINARY_IMAGE = 1 << 9,
    /** The type of the IntermediateResult is "contours". */
    IRUT_CONTOURS = 1 << 10,
    /** The type of the IntermediateResult is "line segments". */
    IRUT_LINE_SEGMENTS = 1 << 11,
    /** The type of the IntermediateResult is "text zones". */
    IRUT_TEXT_ZONES = 1 << 12,
    /** The type of the IntermediateResult is "text removed binary image". */
    IRUT_TEXT_REMOVED_BINARY_IMAGE = 1 << 13,
    /** The type of the IntermediateResult is "candidate barcode zones". */
    IRUT_CANDIDATE_BARCODE_ZONES = 1 << 14,
    /** The type of the IntermediateResult is "localized barcodes". */
    IRUT_LOCALIZED_BARCODES = 1 << 15,
    /** The type of the IntermediateResult is "scaled up barcode image". */
    IRUT_SCALED_UP_BARCODE_IMAGE = 1 << 16,
    /** The type of the IntermediateResult is "deformation resisted barcode image". */
    IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE = 1 << 17,
    /** The type of the IntermediateResult is "complemented barcode image". */
    IRUT_COMPLEMENTED_BARCODE_IMAGE = 1 << 18,
    /** The type of the IntermediateResult is "decoded barcodes". */
    IRUT_DECODED_BARCODES = 1 << 19,
    /** The type of the IntermediateResult is "long lines". */
    IRUT_LONG_LINES = 1 << 20,
    /** The type of the IntermediateResult is "corners". */
    IRUT_CORNERS = 1 << 21,
    /** The type of the IntermediateResult is "candidate quad edges". */
    IRUT_CANDIDATE_QUAD_EDGES = 1 << 22,
    /** The type of the IntermediateResult is "detected quads". */
    IRUT_DETECTED_QUADS = 1 << 23,
    /** The type of the IntermediateResult is "localized text lines". */
    IRUT_LOCALIZED_TEXT_LINES = 1 << 24,
    /** The type of the IntermediateResult is "recognized text lines". */
    IRUT_RECOGNIZED_TEXT_LINES = 1 << 25,
    /** The type of the IntermediateResult is "normalized image". */
    IRUT_NORMALIZED_IMAGE = 1 << 26,
    /** The type of the IntermediateResult is "all". */
    IRUT_ALL = 0x7FFFFFF
};
```
