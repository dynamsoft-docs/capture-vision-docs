---
layout: default-layout
title: Standard Output - Dynamsoft Capture Vision
description: This article is about the standard output in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /architecture/output.html
---

> *Go back to [DCV Architecture](index.md)*

# Output

![DCV Architecture](assets/dcv-architecture-output.png)

As the last piece of the Dynamsoft Capture Vision (DCV) architecture, "output" is responsible for transporting the image-processing results to objects that logically depend on them.

A standard output target is an object that has implemented either the [Captured Result Receiver (CRR) interface](#captured-result-receiver) or [Intermediate Result Receiver (IRR) interface](#intermediate-result-receiver). The two interfaces both consist of multiple callback functions, therefore, a standard output target is usually referred to as a **listening object**.

## Captured Result Receiver

Captured Result Receiver (CRR) is an interface for the output of "final results".

### Final results

Final results refer to the following 6 types of results:

1. The original image
2. Barcode text found on the image
3. Text lines found on the image
4. Document boundaries found on the image
5. Normalized image based on a detected document boundary
6. Data tables parsed from barcode text or text line(s) found on the image

These results are "final" because they are only returned after an image has finished processing. In other words, for each image, the CRR callback functions are only triggered once. 

The CRR interface consists of 

1. A callback function that returns all six types of results. This function is always triggered.
2. Six other callback functions for each of the six types of results. These functions are only triggered when their corresponding types of results exist.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
export interface CapturedResultReceiver {
    /**
     * All results found on the image are returned through this callback.
     * This callback is always triggered.
     */
    onCapturedResultReceived?: (pResult: Core.BasicStructures.CapturedResult) => void;
    /**
     * This callback is only triggered when the raw or original image is set to be returned.
     */
    onRawImageResultReceived?: (pResult: RawImageResultItem) => void;
    /**
     * This callback is only triggered when barcodes are found on the image.
     */
    onDecodedBarcodesReceived?: (pResult: DBR.DecodedBarcodesResult) => void;
    /**
     * This callback is only triggered when text-lines are found on the image.
     */
    onRecognizedTextLinesReceived?: (pResult: DLR.RecognizedTextLinesResult) => void;
    /**
     * This callback is only triggered when document boundary quads are detected on the image.
     */
    onDetectedQuadsReceived?: (pResult: DDN.DetectedQuadsResult) => void;
    /**
     * This callback is only triggered when the image has been normalized successfully.
     */
    onNormalizedImagesReceived?: (pResult: DDN.NormalizedImageResult) => void;
    /**
     * This callback is only triggered when there are parsed results on the image.
     */
    onParsedResultsReceived?: (pResult: DCP.ParsedResult) => void;
}
```
>```java
public interface CapturedResultReceiver {
   /* The callback that contains all results. */
   default void onCapturedResultReceived(CapturedResult result);
   /* The callback that contains only the original raw image. */
   default void onRawImageResultReceived(RawImageResultItem result);
   /* The callback that contains all barcode text found on the image. */
   default void onDecodedBarcodesReceived(DecodedBarcodesResult result);
   /* The callback that contains all text lines found on the image. */
   default void onRecognizedTextLinesReceived(RecognizedTextLinesResult result);
   /* The callback that contains all document boundaries found on the image. */
   default void onDetectedQuadsReceived(DetectedQuadsResult result);
   /* The callback that contains all normalized images. */
   default void onNormalizedImagesReceived(NormalizedImagesResult result);
   /* The callback that contains data tables parsed from barcode text or text line(s) on the image. */
   default void onParsedResultsReceived(ParsedResult result);
}
```
>```objc
@protocol DSCapturedResultReceiver <NSObject>
@required
/* The callback that contains all results. */
- (void)onCapturedResultReceived:(DSCapturedResult*)result;
@optional
/* The callback that contains only the original raw image. */
- (void)onRawImageResultReceived:(DSRawImageResultItem*)result;
/* The callback that contains all barcode text found on the image. */
- (void)onDecodedBarcodesReceived:(DSDecodedBarcodesResult*)result;
/* The callback that contains all text lines found on the image. */
- (void)onRecognizedTextLinesReceived:(DSRecognizedTextLinesResult*)result;
/* The callback that contains all document boundaries found on the image. */
- (void)onDetectedQuadsReceived:(DSDetectedQuadsResult*)result;
/* The callback that contains all normalized images. */
- (void)onNormalizedImagesReceived:(DSNormalizedImagesResult*)result;
/* The callback that contains data tables parsed from barcode text or text line(s) on the image. */
- (void)onParsedResultsReceived:(DSParsedResult*)result;
@end
```
>```swift
protocol IntermediateResultReceiver{
   /* The callback that contains all results. */
   func onCapturedResultReceived(_ result: CapturedResult)
   /* The callback that contains only the original raw image. */
   func onRawImageResultReceived(_ result: RawImageResultItem)
   /* The callback that contains all barcode text found on the image. */
   func onDecodedBarcodesReceived(_ result: DecodedBarcodesResult)
   /* The callback that contains all text lines found on the image. */
   func onRecognizedTextLinesReceived(_ result: RecognizedTextLinesResult)
   /* The callback that contains all document boundaries found on the image. */
   func onDetectedQuadsReceived(_ result: DetectedQuadsResult)
   /* The callback that contains all normalized images. */
   func onNormalizedImagesReceived(_ result: NormalizedImagesResult)
   /* The callback that contains data tables parsed from barcode text or text line(s) on the image. */
   func onParsedResultsReceived(_ result: ParsedResult)
}
```
>
```cpp
class CVR_API CCapturedResultReceiver
{
protected:
    unsigned int observedResultItemTypes;
public:
    CCapturedResultReceiver();
    virtual ~CCapturedResultReceiver();
    unsigned int GetObservedResultItemTypes();
    /**
     * All results found on the image are returned through this callback.
     * This callback is always triggered.
     */
    virtual void OnCapturedResultReceived(const CCapturedResult* pResult);
    /**
     * This callback is only triggered when the raw or original image is set to be returned.
     */
    virtual void OnRawImageResultReceived(const CRawImageResultItem* pResult);
    /**
     * This callback is only triggered when barcodes are found on the image.
     */
    virtual void OnDecodedBarcodesReceived(const dbr::CDecodedBarcodesResult* pResult);
    /**
     * This callback is only triggered when text-lines are found on the image.
     */
    virtual void OnRecognizedTextLinesReceived(const dlr::CRecognizedTextLinesResult* pResult);
    /**
     * This callback is only triggered when document boundary quads are detected on the image.
     */
    virtual void OnDetectedQuadsReceived(const ddn::CDetectedQuadsResult* pResult);
    /**
     * This callback is only triggered when the image has been normalized successfully.
     */
    virtual void OnNormalizedImagesReceived(const ddn::CNormalizedImagesResult* pResult);
    /**
     * This callback is only triggered when there are parsed results on the image.
     */
    virtual void OnParsedResultsReceived(const dcp::CParsedResult* pResult);
};
```

## Intermediate Result Receiver

Intermediate Result Receiver (IRR) is an interface for the output of intermediate results. Intermediate results refer to the following 27 types of results:

### Intermediate results

1. Pre-detected regions unit
2. Localized barcodes unit
3. Decoded barcodes unit
4. Localized text lines unit
5. Recognized text lines unit
6. Detected quads unit
7. Normalized images unit
8. Colour Image unit
9. Down-scaled colour image unit
10. Grayscale image unit
11. Transformed grayscale image unit
12. Enhanced grayscale image unit
13. Binarized image unit
14. Texture detection result unit
15. Texture removed grayscale image unit
16. Texture removed binary image unit
17. Contours unit
18. Line segments unit
19. Text zones unit
20. Text removed binary image unit
21. Long lines unit
22. Corners unit
23. Candidate quad edges unit
24. Candidate barcode zones unit
25. Up-scaled barcode image unit
26. Deformation resisted barcode image unit
27. Complemented barcode image unit

These results are "intermediate" because they are generated while the image is getting processed for the "final" results. For each image, the IRR callback functions are triggered as soon as certain types of results are generated.

> For the JavaScript Edition, due to technical restrictions, these results are returned after the image has finished processing.

The IRR interface consists of 27 callback functions for each of the 27 types of results.
<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
interface IntermediateResultReceiver {
    /**
     * This callback is triggered when regions of interest are pre-detected.
     */
    onPredetectedRegionsReceived?: (targetROIDefName: string,
        taskName: string,
        unit: PredetectedRegionsUnit
    ) => void;
    /**
     * This callback is triggered when barcodes are localized.
     */
    onLocalizedBarcodesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.LocalizedBarcodesUnit) => void;
    /**
     * This callback is triggered when barcodes are decoded.
     */
    onDecodedBarcodesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.DecodedBarcodesUnit) => void;
    /**
     * This callback is triggered when text-lines are localized.
     */
    onLocalizedTextLinesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DLR.IntermediateResult.LocalizedTextLinesUnit) => void;
    /**
     * This callback is triggered when text-lines are recognized.
     */
    onRecognizedTextLinesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DLR.IntermediateResult.RecognizedTextLinesUnit) => void;
    /**
     * This callback is triggered when document boundary quads are detected.
     */
    onDetectedQuadsReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.DetectedQuadsUnit) => void;
    /**
     * This callback is triggered when the image is normalized.
     */
    onNormalizedImagesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.NormalizedImageUnit) => void;
    /**
     * This callback is triggered when a coloured image is produced.
     */
    onColourImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: ColourImageUnit) => void;
    /**
     * This callback is triggered when the coloured images is down-scaled.
     */
    onScaledDownColourImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: ScaledDownColourImageUnit) => void;
    /**
     * This callback is triggered when the coloured images is converted to grayscale.
     */
    onGrayscaleImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: GrayscaleImageUnit) => void;
    /**
     * This callback is triggered when the grayscale image is transformed (usually this means all the pixels have their colour inverted).
     */
    onTransformedGrayscaleImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TransformedGrayscaleImageUnit) => void;
    /**
     * This callback is triggered when the quality of the grayscale image is enhanced.
     */
    onEnhancedGrayscaleImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: EnhancedGrayscaleImageUnit) => void;
    /**
     * This callback is triggered when the grayscale image is binarized.
     */
    onBinaryImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: BinaryImageUnit) => void;
    /**
     * This callback is triggered when texture is detected on the image.
     */
    onTextureDetectionResultUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextureDetectionResultUnit) => void;
    /**
     * This callback is triggered when texture is removed from the grayscale image.
     */
    onTextureRemovedGrayscaleImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextureRemovedGrayscaleImageUnit) => void;
    /**
     * This callback is triggered when texture is removed from the binary image.
     */
    onTextureRemovedBinaryImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextureRemovedBinaryImageUnit) => void;
    /**
     * This callback is triggered when contours are found on the image.
     */
    onContoursUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: ContoursUnit) => void;
    /**
     * This callback is triggered when line segments are found on the image.
     */
    onLineSegmentsUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: LineSegmentsUnit) => void;
    /**
     * This callback is triggered when text zones are found on the image.
     */
    onTextZonesUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextZonesUnit) => void;
    /**
     * This callback is triggered when an image without text is produced.
     */
    onTextRemovedBinaryImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextRemovedBinaryImageUnit) => void;
    /**
     * This callback is triggered when long lines are found on the image.
     */
    onLongLinesUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.LongLinesUnit) => void;
    /**
     * This callback is triggered when corners are found on the image.
     */
    onCornersUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.CornersUnit) => void;
    /**
     * This callback is triggered when candidate quad edges are found on the image.
     */
    onCandidateQuadEdgesUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.CandidateQuadEdgesUnit) => void;
    /**
     * This callback is triggered when candidate barcode zones are found on the image.
     */
    onCandidateBarcodeZonesUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.CandidateBarcodeZonesUnit) => void;
    /**
     * This callback is triggered when the barcode zones are up-scaled for better decoding.
     */
    onScaledUpBarcodeImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.ScaledUpBarcodeImageUnit) => void;
    /**
     * This callback is triggered when deformation of the barcode zones is corrected.
     */
    onDeformationResistedBarcodeImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.DeformationResistedBarcodeImageUnit) => void;
    /**
     * This callback is triggered when the barcode zones are complemented for better decoding.
     */
    onComplementedBarcodeImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.ComplementedBarcodeImageUnit) => void;
}
```
>
```java
public interface IntermediateResultReceiver {
    default void onPredetectedRegionsReceived(String targetROIDefName, String taskName, PredetectedRegionsUnit unit);
    default void onLocalizedBarcodesReceived(String targetROIDefName, String taskName, LocalizedBarcodesUnit unit);
    default void onDecodedBarcodesReceived(String targetROIDefName, String taskName, DecodedBarcodesUnit unit);
    default void onLocalizedTextLinesReceived(String targetROIDefName, String taskName, LocalizedBarcodesUnit unit);
    default void onRecognizedTextLinesReceived(String targetROIDefName, String taskName, RecognizedTextLinesUnit unit);
    default void onDetectedQuadsReceived(String targetROIDefName, String taskName, DetectedQuadsUnit unit);
    default void onNormalizedImagesReceived(String targetROIDefName, String taskName, NormalizedImageUnit unit);
    default void onColourImageUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, ColourImageUnit unit);
    default void onScaledDownColourImageUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, ScaledDownColourImageUnit unit);
    default void onGrayscaleImageUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, GrayscaleImageUnit unit);
    default void onTransformedGrayscaleImageUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, TransformedGrayscaleImageUnit unit);
    default void onEnhancedGrayscaleImageUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, EnhancedGrayscaleImageUnit unit);
    default void onBinaryImageUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, BinaryImageUnit unit);
    default void onTextureDetectionResultUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, TextureDetectionResultUnit unit);
    default void onTextureRemovedGrayscaleImageUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, extureRemovedGrayscaleImageUnit unit);
    default void onTextureRemovedBinaryImageUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, TextureRemovedBinaryImageUnit unit);
    default void onContoursUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, ContoursUnit unit);
    default void onLineSegmentsUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, LineSegmentsUnit unit);
    default void onTextZonesUnitReceived(String targetROIDefName, String taskName, SectionType sectionType, TextZonesUnit unit);
    default void onTextRemovedBinaryImageUnitReceived(String targetROIDefName, String taskName, SectionType sectionType,
    TextRemovedBinaryImageUnit unit);
    default void onLongLinesUnitReceived(String targetROIDefName, String taskName, LongLinesUnit unit);
    default void onCornersUnitReceived(String targetROIDefName, String taskName, CornersUnit unit);
    default void onCandidateQuadEdgesUnitReceived(String targetROIDefName, String taskName, CandidateQuadEdgesUnit unit);
    default void onCandidateBarcodeZonesUnitReceived(String targetROIDefName, String taskName, CandidateBarcodeZonesUnit unit);
    default void onScaledUpBarcodeImageUnitReceived(String targetROIDefName, String taskName, ScaledUpBarcodeImageUnit unit);
    default void onDeformationResistedBarcodeImageUnitReceived(String targetROIDefName, String taskName, DeformationResistedBarcodeImageUnit unit);
    default void onComplementedBarcodeImageUnitReceived(String targetROIDefName, String taskName, ComplementedBarcodeImageUnit unit);
}
```
>
```objc
@protocol DSIntermediateResultReceiver <NSObject>
@optional
/** Receive colour images when they are output by the library. */
- (void)onColourImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSColourImageUnit*) unit;
/** Receive scaled down colour images when they are output by the library. */
- (void)onScaledDownColourImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSScaledDownColourImageUnit*) unit;
/** Receive grayscale image when they are output by the library. */
- (void)onGrayscaleImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSGrayscaleImageUnit*) unit;
/** Receive transformed grayscale (colour inverted) image when they are output by the library. */
- (void)onTransformedGrayscaleImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSTransformedGrayscaleImageUnit*) unit;
/** Receive predetected region when they are output by the library. */
- (void)onPredetectedRegionsReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSPredetectedRegionsUnit*) unit;
/** Receive enhanced grayscale image when they are output by the library. */
- (void)onEnhancedGrayscaleImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSEnhancedGrayscaleImageUnit*) unit;
/** Receive binary image when they are output by the library. */
- (void)onBinaryImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSBinaryImageUnit*) unit;
/** Receive texture detection result when they are output by the library. */
- (void)onTextureDetectionResultUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSTextureDetectionResultUnit*) unit;
/** Receive grayscale image without texture when they are output by the library. */
- (void)onTextureRemovedGrayscaleImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSTextureRemovedGrayscaleImageUnit*) unit;
/** Receive binary image without texture when they are output by the library. */
- (void)onTextureRemovedBinaryImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSTextureRemovedBinaryImageUnit*) unit;
/** Receive binary image without text when they are output by the library. */
- (void)onTextRemovedBinaryImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSTextRemovedBinaryImageUnit*) unit;
/** Receive contours when they are detected by the library. */
- (void)onContoursUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSContoursUnit*) unit;
/** Receive line segments when they are detected by the library. */
- (void)onLineSegmentsUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSLineSegmentsUnit*) unit;
/** Receive the quadrilaterals of canditate barcode zones when they are detected by the library. */
- (void)onCandidateBarcodeZonesUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSCandidateBarcodeZonesUnit *) unit;
/** Receive the localization results of the barcodes when they are detected by the library. */
- (void)onLocalizedBarcodesReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSLocalizedBarcodesUnit *) unit;
/** Receive scaled up images of the barcodes when barcode zones are scaled up. */
- (void)onScaledUpBarcodeImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSScaledUpBarcodeImageUnit *) unit;
/** Receive images of the barcodes when deformed barcode zones are resisted. */
- (void)onDeformationResistedBarcodeImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSDeformationResistedBarcodeImageUnit *) unit;
/** Receive images of the barcodes when incompleted barcode zones are completed. */
- (void)onComplementedBarcodeImageUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSComplementedBarcodeImageUnit *) unit;
/** Receive DSDecodedBarcodesUnit when barcodes are decoded. */
- (void)onDecodedBarcodesReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSDecodedBarcodesUnit *) unit;
/** Receive text zones info when they are located. */
- (void)onTextZonesUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    sectiontype:(DSSectionType) sectionType
    unit:(DSTextZonesUnit*) unit;
/** Receive text lines info when they are located. */
- (void)onLocalizedTextLinesReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSLocalizedTextLinesUnit *) unit;
/** Receive text line info when they are recognized. */
- (void)onRecognizedTextLinesReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSRecognizedTextLinesUnit *) unit;
/** Receive long line units when they are detected. Based on the long lines, the library can find the corners of the quadrilateral. */
- (void)onLongLinesUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSLongLinesUnit *) unit;
/** Receive corners unit when they are detected. Based on the corners, the library can find the edges of the quadrilateral. */
- (void)onCornersUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSCornersUnit *) unit;
/** Receive quad edges unit when they are detected. Based on the edges, the library can finally confirm the vertex coordinates of the quadrilateral. */
- (void)onCandidateQuadEdgesUnitReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSCandidateQuadEdgesUnit *) unit;
/** Receive detected quadrilaterals when they are detected. */
- (void)onDetectedQuadsReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSDetectedQuadsUnit *) unit;
/** Receive normalized images when they are output. */
- (void)onNormalizedImagesReceived:(NSString*) targetROIDefName
    taskName:(NSString*) taskName
    unit:(DSNormalizedImageUnit *) unit;
@end
```
>
```swift
protocol IntermediateResultReceiver{
   /** Receive colour images when they are output by the library. */
   func onColourImageUnitReceived(_ targetROIDefName: String, taskName:string, sectionType: SectionType, unit: ColourImageUnit)
   /** Receive scaled down colour images when they are output by the library. */
   func onScaledDownColourImageUnitReceived(_ targetROIDefName: String, taskName: String, sectionType: SectionType, unit: ScaledDownColourImageUnit)
   /** Receive grayscale image when they are output by the library. */
   func onGrayscaleImageUnitReceived(_ targetROIDefName: String, taskName:string, sectionType: SectionType, unit: GrayscaleImageUnit)
   /** Receive transformed grayscale (colour inverted) image when they are output by the library. */
   func onTransformedGrayscaleImageUnitReceived(_ targetROIDefName: String, taskName: String, sectionType: SectionType, unit: TransformedGrayscaleImageUnit)
   /** Receive predetected region when they are output by the library. */
   func onPredetectedRegionsReceived(_ targetROIDefName: String, taskName:string, unit: PredetectedRegionsUnit)
   /** Receive enhanced grayscale image when they are output by the library. */
   func onEnhancedGrayscaleImageUnitReceived(_ targetROIDefName: String, taskName: String, sectionType: SectionType, unit: EnhancedGrayscaleImageUnit)
   /** Receive binary image when they are output by the library. */
   func onBinaryImageUnitReceived(_ targetROIDefName: String, taskName:string, sectionType: SectionType, unit: BinaryImageUnit)
   /** Receive texture detection result when they are output by the library. */
   func onTextureDetectionResultUnitReceived(_ targetROIDefName: String, taskName: String, sectionType: SectionType, unit: TextureDetectionResultUnit)
   /** Receive grayscale image without texture when they are output by the library. */
   func onTextureRemovedGrayscaleImageUnitReceived(_ targetROIDefName: String, taskName: String, sectionType: SectionType, unit: TextureRemovedGrayscaleImageUnit)
   /** Receive binary image without texture when they are output by the library. */
   func onTextureRemovedBinaryImageUnitReceived(_ targetROIDefName: String, taskName: String, sectionType: SectionType, unit: TextureRemovedBinaryImageUnit)
   /** Receive binary image without text when they are output by the library. */
   func onTextRemovedBinaryImageUnitReceived(_ targetROIDefName: String, taskName: String, sectionType: SectionType, unit: TextRemovedBinaryImageUnit)
   /** Receive contours when they are detected by the library. */
   func onContoursUnitReceived(_ targetROIDefName: String, taskName:string, sectionType: SectionType, unit: ContoursUnit)
   /** Receive line segments when they are detected by the library. */
   func onLineSegmentsUnitReceived(_ targetROIDefName: String, taskName:string, sectionType: SectionType, unit: LineSegmentsUnit)
   /** Receive the quadrilaterals of canditate barcode zones when they are detected by the library. */
   func onCandidateBarcodeZonesUnitReceived(_ targetROIDefName: String, taskName: String, unit: CandidateBarcodeZonesUnit)
   /** Receive the localization results of the barcodes when they are detected by the library. */
   func onLocalizedBarcodesReceived(_ targetROIDefName: String, taskName:string, unit: LocalizedBarcodesUnit)
   /** Receive scaled up images of the barcodes when barcode zones are scaled up. */
   func onScaledUpBarcodeImageUnitReceived(_ targetROIDefName: String, taskName:string, unit: ScaledUpBarcodeImageUnit)
   /** Receive images of the barcodes when deformed barcode zones are resisted. */
   func onDeformationResistedBarcodeImageUnitReceived(_ targetROIDefName: String, taskName: String, unit: DeformationResistedBarcodeImageUnit)
   /** Receive images of the barcodes when incompleted barcode zones are completed. */
   func onComplementedBarcodeImageUnitReceived(_ targetROIDefName: String, taskName: String, unit: ComplementedBarcodeImageUnit)
   /** Receive DSDecodedBarcodesUnit when barcodes are decoded. */
   func onDecodedBarcodesReceived(_ targetROIDefName: String, taskName:string, unit: DecodedBarcodesUnit)
   /** Receive text zones info when they are located. */
   func onTextZonesUnitReceived(_ targetROIDefName: String, taskName:string, sectionType: SectionType, unit: TextZonesUnit)
   /** Receive text lines info when they are located. */
   func onLocalizedTextLinesReceived(_ targetROIDefName: String, taskName:string, unit: LocalizedTextLinesUnit)
   /** Receive text line info when they are recognized. */
   func onRecognizedTextLinesReceived(_ targetROIDefName: String, taskName:string, unit: RecognizedTextLinesUnit)
   /** Receive long line units when they are detected. Based on the long lines, the library can find the corners of the quadrilateral. */
   func onLongLinesUnitReceived(_ targetROIDefName: String, taskName:string, unit: LongLinesUnit)
   /** Receive corners unit when they are detected. Based on the corners, the library    can find the edges of the quadrilateral. */
   func onCornersUnitReceived(_ targetROIDefName: String, taskName:string, unit: CornersUnit)
   /** Receive quad edges unit when they are detected. Based on the edges, the library can finally confirm the vertex coordinates of the quadrilateral. */
   func onCandidateQuadEdgesUnitReceived(_ targetROIDefName: String, taskName:string, unit: CandidateQuadEdgesUnit)
   /** Receive detected quadrilaterals when they are detected. */
   func onDetectedQuadsReceived(_ targetROIDefName: String, taskName:string, unit: DetectedQuadsUnit)
   /** Receive normalized images when they are output. */
   func onNormalizedImagesReceived(_ targetROIDefName: String, taskName:string, unit: NormalizedImageUnit)
}
```
>
```cpp
        class CIntermediateResultReceiver
        {
        protected:
            unsigned long long observedResultUnitTypes;
            int resultLevel;
        public:
            CIntermediateResultReceiver();
            CIntermediateResultReceiver(int _level);
            virtual ~CIntermediateResultReceiver(){};
            unsigned long long GetObservedResultUnitTypes();
            int GetResultLevel();
            virtual void OnPredetectedRegionsReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const CPredetectedRegionsUnit *pResult);
            virtual void OnLocalizedBarcodesReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dbr::intermediate_results::CLocalizedBarcodesUnit *pResult);
            virtual void OnDecodedBarcodesReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dbr::intermediate_results::CDecodedBarcodesUnit *pResult);
            virtual void OnLocalizedTextLinesReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dlr::intermediate_results::CLocalizedTextLinesUnit *pResult);
            virtual void OnRecognizedTextLinesReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dlr::intermediate_results::CRecognizedTextLinesUnit *pResult);
            virtual void OnDetectedQuadsReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const ddn::intermediate_results::CDetectedQuadsUnit *pResult);
            virtual void OnNormalizedImagesReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const ddn::intermediate_results::CNormalizedImageUnit *pResult);
            virtual void OnColourImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CColourImageUnit *pResult);
            virtual void OnScaledDownColourImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CScaledDownColourImageUnit *pResult);
            virtual void OnGrayscaleImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CGrayscaleImageUnit *pResult);
            virtual void OnTransformedGrayscaleImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CTransformedGrayscaleImageUnit *pResult);
            virtual void OnEnhancedGrayscaleImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CEnhancedGrayscaleImageUnit *pResult);
            virtual void OnBinaryImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CBinaryImageUnit *pResult);
            virtual void OnTextureDetectionResultUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CTextureDetectionResultUnit *pResult);
            virtual void OnTextureRemovedGrayscaleImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CTextureRemovedGrayscaleImageUnit *pResult);
            virtual void OnTextureRemovedBinaryImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CTextureRemovedBinaryImageUnit *pResult);
            virtual void OnContoursUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CContoursUnit *pResult);
            virtual void OnLineSegmentsUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CLineSegmentsUnit *pResult);
            virtual void OnTextZonesUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType, 
                                                    const CTextZonesUnit *pResult);
            virtual void OnTextRemovedBinaryImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    SectionType sectionType,
                                                    const CTextRemovedBinaryImageUnit *pResult);
            virtual void OnLongLinesUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const ddn::intermediate_results::CLongLinesUnit *pResult);
            virtual void OnCornersUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const ddn::intermediate_results::CCornersUnit *pResult);
            virtual void OnCandidateQuadEdgesUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const ddn::intermediate_results::CCandidateQuadEdgesUnit *pResult);
            virtual void OnCandidateBarcodeZonesUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dbr::intermediate_results::CCandidateBarcodeZonesUnit *pResult);
            virtual void OnScaledUpBarcodeImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dbr::intermediate_results::CScaledUpBarcodeImageUnit *pResult);
            virtual void OnDeformationResistedBarcodeImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dbr::intermediate_results::CDeformationResistedBarcodeImageUnit *pResult);
            virtual void OnComplementedBarcodeImageUnitReceived(const char* targetROIDefName, 
                                                    const char* taskName, 
                                                    const dbr::intermediate_results::CComplementedBarcodeImageUnit *pResult);
        };
```
