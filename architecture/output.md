---
layout: default-layout
title: Standard Output - Dynamsoft Capture Vision Architecture
description: This article is about the standard output in the Dynamsoft Capture Vision architecture.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /architecture/output.html
---

> *Go to [DCV Architecture](index.md)*

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
interface CapturedResultReceiver {
    /**
     * All results found on the image are returned through this callback.
     * This callback is always triggered.
     */
    onCapturedResultReceived?: (pResult: Core.BasicStructures.CapturedResult) => void;
    /**
     * This callback is only triggered when the raw or original image is set to be returned.
     */
    onOriginalImageResultReceived?: (pResult: OriginalImageResultItem) => void;
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
   default void onOriginalImageResultReceived(OriginalImageResultItem result);
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
- (void)onOriginalImageResultReceived:(DSOriginalImageResultItem*)result;
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
   func onOriginalImageResultReceived(_ result: OriginalImageResultItem)
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
    virtual void OnOriginalImageResultReceived(const COriginalImageResultItem* pResult);
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
    onTaskResultsReceived?: (result: IntermediateResult,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when regions of interest are pre-detected.
     */
    onPredetectedRegionsReceived?: (unit: PredetectedRegionsUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when barcodes are localized.
     */
    onLocalizedBarcodesReceived?: (unit: DBR.IntermediateResult.LocalizedBarcodesUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when barcodes are decoded.
     */
    onDecodedBarcodesReceived?: (unit: DBR.IntermediateResult.DecodedBarcodesUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when text-lines are localized.
     */
    onLocalizedTextLinesReceived?: (unit: DLR.IntermediateResult.LocalizedTextLinesUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when text-lines are recognized.
     */
    onRecognizedTextLinesReceived?: (unit: DLR.IntermediateResult.RecognizedTextLinesUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when document boundary quads are detected.
     */
    onDetectedQuadsReceived?: (unit: DDN.IntermediateResult.DetectedQuadsUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when the image is normalized.
     */
    onNormalizedImagesReceived?: (unit: DDN.IntermediateResult.NormalizedImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when a coloured image is produced.
     */
    onColourImageUnitReceived?: (unit: ColourImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when the coloured images is down-scaled.
     */
    onScaledDownColourImageUnitReceived?: (unit: ScaledDownColourImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when the coloured images is converted to grayscale.
     */
    onGrayscaleImageUnitReceived?: (unit: GrayscaleImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when the grayscale image is transformed (usually this means all the pixels have their colour inverted).
     */
    onTransformedGrayscaleImageUnitReceived?: (unit: TransformedGrayscaleImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when the quality of the grayscale image is enhanced.
     */
    onEnhancedGrayscaleImageUnitReceived?: (unit: EnhancedGrayscaleImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when the grayscale image is binarized.
     */
    onBinaryImageUnitReceived?: (unit: BinaryImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when texture is detected on the image.
     */
    onTextureDetectionResultUnitReceived?: (unit: TextureDetectionResultUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when texture is removed from the grayscale image.
     */
    onTextureRemovedGrayscaleImageUnitReceived?: (unit: TextureRemovedGrayscaleImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when texture is removed from the binary image.
     */
    onTextureRemovedBinaryImageUnitReceived?: (unit: TextureRemovedBinaryImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when contours are found on the image.
     */
    onContoursUnitReceived?: (unit: ContoursUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when line segments are found on the image.
     */
    onLineSegmentsUnitReceived?: (unit: LineSegmentsUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when text zones are found on the image.
     */
    onTextZonesUnitReceived?: (unit: TextZonesUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when an image without text is produced.
     */
    onTextRemovedBinaryImageUnitReceived?: (unit: TextRemovedBinaryImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when long lines are found on the image.
     */
    onLongLinesUnitReceived?: (unit: DDN.IntermediateResult.LongLinesUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when corners are found on the image.
     */
    onCornersUnitReceived?: (unit: DDN.IntermediateResult.CornersUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when candidate quad edges are found on the image.
     */
    onCandidateQuadEdgesUnitReceived?: (unit: DDN.IntermediateResult.CandidateQuadEdgesUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when candidate barcode zones are found on the image.
     */
    onCandidateBarcodeZonesUnitReceived?: (unit: DBR.IntermediateResult.CandidateBarcodeZonesUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when the barcode zones are up-scaled for better decoding.
     */
    onScaledUpBarcodeImageUnitReceived?: (unit: DBR.IntermediateResult.ScaledUpBarcodeImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when deformation of the barcode zones is corrected.
     */
    onDeformationResistedBarcodeImageUnitReceived?: (unit: DBR.IntermediateResult.DeformationResistedBarcodeImageUnit,
        info: IntermediateResultExtraInfo) => void;
    /**
     * This callback is triggered when the barcode zones are complemented for better decoding.
     */
    onComplementedBarcodeImageUnitReceived?: (unit: DBR.IntermediateResult.ComplementedBarcodeImageUnit,
        info: IntermediateResultExtraInfo) => void;
}
```
>
```java
public interface IntermediateResultReceiver {
    default void onTaskResultsReceived(IntermediateResult result, IntermediateResultExtraInfo info);
    default void onPredetectedRegionsReceived(PredetectedRegionsUnit unit, IntermediateResultExtraInfo info);
    default void onLocalizedBarcodesReceived(LocalizedBarcodesUnit unit, IntermediateResultExtraInfo info);
    default void onDecodedBarcodesReceived(DecodedBarcodesUnit unit, IntermediateResultExtraInfo info);
    default void onLocalizedTextLinesReceived(LocalizedBarcodesUnit unit, IntermediateResultExtraInfo info);
    default void onRecognizedTextLinesReceived(RecognizedTextLinesUnit unit, IntermediateResultExtraInfo info);
    default void onDetectedQuadsReceived(DetectedQuadsUnit unit, IntermediateResultExtraInfo info);
    default void onNormalizedImagesReceived(NormalizedImageUnit unit, IntermediateResultExtraInfo info);
    default void onColourImageUnitReceived(ColourImageUnit unit, IntermediateResultExtraInfo info);
    default void onScaledDownColourImageUnitReceived(ScaledDownColourImageUnit unit, IntermediateResultExtraInfo info);
    default void onGrayscaleImageUnitReceived(GrayscaleImageUnit unit, IntermediateResultExtraInfo info);
    default void onTransformedGrayscaleImageUnitReceived(TransformedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
    default void onEnhancedGrayscaleImageUnitReceived(EnhancedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
    default void onBinaryImageUnitReceived(BinaryImageUnit unit, IntermediateResultExtraInfo info);
    default void onTextureDetectionResultUnitReceived(TextureDetectionResultUnit unit, IntermediateResultExtraInfo info);
    default void onTextureRemovedGrayscaleImageUnitReceived(extureRemovedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
    default void onTextureRemovedBinaryImageUnitReceived(TextureRemovedBinaryImageUnit unit, IntermediateResultExtraInfo info);
    default void onContoursUnitReceived(ContoursUnit unit, IntermediateResultExtraInfo info);
    default void onLineSegmentsUnitReceived(LineSegmentsUnit unit, IntermediateResultExtraInfo info);
    default void onTextZonesUnitReceived(TextZonesUnit unit, IntermediateResultExtraInfo info);
    default void onTextRemovedBinaryImageUnitReceived(TextRemovedBinaryImageUnit unit, IntermediateResultExtraInfo info);
    default void onLongLinesUnitReceived(LongLinesUnit unit, IntermediateResultExtraInfo info);
    default void onCornersUnitReceived(CornersUnit unit, IntermediateResultExtraInfo info);
    default void onCandidateQuadEdgesUnitReceived(CandidateQuadEdgesUnit unit, IntermediateResultExtraInfo info);
    default void onCandidateBarcodeZonesUnitReceived(CandidateBarcodeZonesUnit unit, IntermediateResultExtraInfo info);
    default void onScaledUpBarcodeImageUnitReceived(ScaledUpBarcodeImageUnit unit, IntermediateResultExtraInfo info);
    default void onDeformationResistedBarcodeImageUnitReceived(DeformationResistedBarcodeImageUnit unit, IntermediateResultExtraInfo info);
    default void onComplementedBarcodeImageUnitReceived(ComplementedBarcodeImageUnit unit, IntermediateResultExtraInfo info);
}
```
>
```objc
@protocol DSIntermediateResultReceiver <NSObject>
@optional
- (void)onTaskResultsReceived:(DSIntermediateResult*) result info:(IntermediateResultExtraInfo*)info;
/** Receive colour images when they are output by the library. */
- (void)onColourImageUnitReceived:(DSColourImageUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive scaled down colour images when they are output by the library. */
- (void)onScaledDownColourImageUnitReceived:(DSScaledDownColourImageUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive grayscale image when they are output by the library. */
- (void)onGrayscaleImageUnitReceived:(DSGrayscaleImageUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive transformed grayscale (colour inverted) image when they are output by the library. */
- (void)onTransformedGrayscaleImageUnitReceived:(DSTransformedGrayscaleImageUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive predetected region when they are output by the library. */
- (void)onPredetectedRegionsReceived:(DSPredetectedRegionsUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive enhanced grayscale image when they are output by the library. */
- (void)onEnhancedGrayscaleImageUnitReceived:(DSEnhancedGrayscaleImageUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive binary image when they are output by the library. */
- (void)onBinaryImageUnitReceived:(DSBinaryImageUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive texture detection result when they are output by the library. */
- (void)onTextureDetectionResultUnitReceived:(DSTextureDetectionResultUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive grayscale image without texture when they are output by the library. */
- (void)onTextureRemovedGrayscaleImageUnitReceived:(DSTextureRemovedGrayscaleImageUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive binary image without texture when they are output by the library. */
- (void)onTextureRemovedBinaryImageUnitReceived:(DSTextureRemovedBinaryImageUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive binary image without text when they are output by the library. */
- (void)onTextRemovedBinaryImageUnitReceived:(DSTextRemovedBinaryImageUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive contours when they are detected by the library. */
- (void)onContoursUnitReceived:(DSContoursUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive line segments when they are detected by the library. */
- (void)onLineSegmentsUnitReceived:(DSLineSegmentsUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive the quadrilaterals of canditate barcode zones when they are detected by the library. */
- (void)onCandidateBarcodeZonesUnitReceived:(DSCandidateBarcodeZonesUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive the localization results of the barcodes when they are detected by the library. */
- (void)onLocalizedBarcodesReceived:(DSLocalizedBarcodesUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive scaled up images of the barcodes when barcode zones are scaled up. */
- (void)onScaledUpBarcodeImageUnitReceived:(DSScaledUpBarcodeImageUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive images of the barcodes when deformed barcode zones are resisted. */
- (void)onDeformationResistedBarcodeImageUnitReceived:(DSDeformationResistedBarcodeImageUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive images of the barcodes when incompleted barcode zones are completed. */
- (void)onComplementedBarcodeImageUnitReceived:(DSComplementedBarcodeImageUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive DSDecodedBarcodesUnit when barcodes are decoded. */
- (void)onDecodedBarcodesReceived:(DSDecodedBarcodesUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive text zones info when they are located. */
- (void)onTextZonesUnitReceived:(DSTextZonesUnit*) unit info:(IntermediateResultExtraInfo*)info;
/** Receive text lines info when they are located. */
- (void)onLocalizedTextLinesReceived:(DSLocalizedTextLinesUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive text line info when they are recognized. */
- (void)onRecognizedTextLinesReceived:(DSRecognizedTextLinesUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive long line units when they are detected. Based on the long lines, the library can find the corners of the quadrilateral. */
- (void)onLongLinesUnitReceived:(DSLongLinesUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive corners unit when they are detected. Based on the corners, the library can find the edges of the quadrilateral. */
- (void)onCornersUnitReceived:(DSCornersUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive quad edges unit when they are detected. Based on the edges, the library can finally confirm the vertex coordinates of the quadrilateral. */
- (void)onCandidateQuadEdgesUnitReceived:(DSCandidateQuadEdgesUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive detected quadrilaterals when they are detected. */
- (void)onDetectedQuadsReceived:(DSDetectedQuadsUnit *) unit info:(IntermediateResultExtraInfo*)info;
/** Receive normalized images when they are output. */
- (void)onNormalizedImagesReceived:(DSNormalizedImageUnit *) unit info:(IntermediateResultExtraInfo*)info;
@end
```
>
```swift
protocol IntermediateResultReceiver{
   func onTaskResultsReceived(_ result: IntermediateResult, info: IntermediateResultExtraInfo)
   /** Receive colour images when they are output by the library. */
   func onColourImageUnitReceived(_ unit: ColourImageUnit, info: IntermediateResultExtraInfo)
   /** Receive scaled down colour images when they are output by the library. */
   func onScaledDownColourImageUnitReceived(_ unit: ScaledDownColourImageUnit, info: IntermediateResultExtraInfo)
   /** Receive grayscale image when they are output by the library. */
   func onGrayscaleImageUnitReceived(_ unit: GrayscaleImageUnit, info: IntermediateResultExtraInfo)
   /** Receive transformed grayscale (colour inverted) image when they are output by the library. */
   func onTransformedGrayscaleImageUnitReceived(_ unit: TransformedGrayscaleImageUnit, info: IntermediateResultExtraInfo)
   /** Receive predetected region when they are output by the library. */
   func onPredetectedRegionsReceived(_ unit: PredetectedRegionsUnit, info: IntermediateResultExtraInfo)
   /** Receive enhanced grayscale image when they are output by the library. */
   func onEnhancedGrayscaleImageUnitReceived(_ unit: EnhancedGrayscaleImageUnit, info: IntermediateResultExtraInfo)
   /** Receive binary image when they are output by the library. */
   func onBinaryImageUnitReceived(_ unit: BinaryImageUnit, info: IntermediateResultExtraInfo)
   /** Receive texture detection result when they are output by the library. */
   func onTextureDetectionResultUnitReceived(_ unit: TextureDetectionResultUnit, info: IntermediateResultExtraInfo)
   /** Receive grayscale image without texture when they are output by the library. */
   func onTextureRemovedGrayscaleImageUnitReceived(_ unit: TextureRemovedGrayscaleImageUnit, info: IntermediateResultExtraInfo)
   /** Receive binary image without texture when they are output by the library. */
   func onTextureRemovedBinaryImageUnitReceived(_ unit: TextureRemovedBinaryImageUnit, info: IntermediateResultExtraInfo)
   /** Receive binary image without text when they are output by the library. */
   func onTextRemovedBinaryImageUnitReceived(_ unit: TextRemovedBinaryImageUnit, info: IntermediateResultExtraInfo)
   /** Receive contours when they are detected by the library. */
   func onContoursUnitReceived(_ unit: ContoursUnit, info: IntermediateResultExtraInfo)
   /** Receive line segments when they are detected by the library. */
   func onLineSegmentsUnitReceived(_ unit: LineSegmentsUnit, info: IntermediateResultExtraInfo)
   /** Receive the quadrilaterals of canditate barcode zones when they are detected by the library. */
   func onCandidateBarcodeZonesUnitReceived(_ unit: CandidateBarcodeZonesUnit, info: IntermediateResultExtraInfo)
   /** Receive the localization results of the barcodes when they are detected by the library. */
   func onLocalizedBarcodesReceived(_ unit: LocalizedBarcodesUnit, info: IntermediateResultExtraInfo)
   /** Receive scaled up images of the barcodes when barcode zones are scaled up. */
   func onScaledUpBarcodeImageUnitReceived(_ unit: ScaledUpBarcodeImageUnit, info: IntermediateResultExtraInfo)
   /** Receive images of the barcodes when deformed barcode zones are resisted. */
   func onDeformationResistedBarcodeImageUnitReceived(_ unit: DeformationResistedBarcodeImageUnit, info: IntermediateResultExtraInfo)
   /** Receive images of the barcodes when incompleted barcode zones are completed. */
   func onComplementedBarcodeImageUnitReceived(_ unit: ComplementedBarcodeImageUnit, info: IntermediateResultExtraInfo)
   /** Receive DSDecodedBarcodesUnit when barcodes are decoded. */
   func onDecodedBarcodesReceived(_ unit: DecodedBarcodesUnit, info: IntermediateResultExtraInfo)
   /** Receive text zones info when they are located. */
   func onTextZonesUnitReceived(_ unit: TextZonesUnit, info: IntermediateResultExtraInfo)
   /** Receive text lines info when they are located. */
   func onLocalizedTextLinesReceived(_ unit: LocalizedTextLinesUnit, info: IntermediateResultExtraInfo)
   /** Receive text line info when they are recognized. */
   func onRecognizedTextLinesReceived(_ unit: RecognizedTextLinesUnit, info: IntermediateResultExtraInfo)
   /** Receive long line units when they are detected. Based on the long lines, the library can find the corners of the quadrilateral. */
   func onLongLinesUnitReceived(_ unit: LongLinesUnit, info: IntermediateResultExtraInfo)
   /** Receive corners unit when they are detected. Based on the corners, the library    can find the edges of the quadrilateral. */
   func onCornersUnitReceived(_ unit: CornersUnit, info: IntermediateResultExtraInfo)
   /** Receive quad edges unit when they are detected. Based on the edges, the library can finally confirm the vertex coordinates of the quadrilateral. */
   func onCandidateQuadEdgesUnitReceived(_ unit: CandidateQuadEdgesUnit, info: IntermediateResultExtraInfo)
   /** Receive detected quadrilaterals when they are detected. */
   func onDetectedQuadsReceived(_ unit: DetectedQuadsUnit, info: IntermediateResultExtraInfo)
   /** Receive normalized images when they are output. */
   func onNormalizedImagesReceived(_ unit: NormalizedImageUnit, info: IntermediateResultExtraInfo)
}
```
>
```cpp
class CIntermediateResultReceiver
{
public:
    CIntermediateResultReceiver();
    virtual ~CIntermediateResultReceiver(){};
    CObservationParameters* GetObservationParameters();
    virtual void OnTaskResultsReceived(const CIntermediateResult* pResult, const IntermediateResultExtraInfo* info);
    virtual void OnPredetectedRegionsReceived(CPredetectedRegionsUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnLocalizedBarcodesReceived(dbr::intermediate_results::CLocalizedBarcodesUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnDecodedBarcodesReceived(dbr::intermediate_results::CDecodedBarcodesUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnLocalizedTextLinesReceived(dlr::intermediate_results::CLocalizedTextLinesUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnRecognizedTextLinesReceived(dlr::intermediate_results::CRecognizedTextLinesUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnDetectedQuadsReceived(ddn::intermediate_results::CDetectedQuadsUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnNormalizedImagesReceived(ddn::intermediate_results::CNormalizedImagesUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnColourImageUnitReceived(CColourImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnScaledDownColourImageUnitReceived(CScaledDownColourImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnGrayscaleImageUnitReceived(CGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnTransformedGrayscaleImageUnitReceived(CTransformedGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnEnhancedGrayscaleImageUnitReceived(CEnhancedGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnBinaryImageUnitReceived(CBinaryImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnTextureDetectionResultUnitReceived(CTextureDetectionResultUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnTextureRemovedGrayscaleImageUnitReceived(CTextureRemovedGrayscaleImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnTextureRemovedBinaryImageUnitReceived(CTextureRemovedBinaryImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnContoursUnitReceived(CContoursUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnLineSegmentsUnitReceived(CLineSegmentsUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnTextZonesUnitReceived(CTextZonesUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnTextRemovedBinaryImageUnitReceived(CTextRemovedBinaryImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnLongLinesUnitReceived(ddn::intermediate_results::CLongLinesUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnCornersUnitReceived(ddn::intermediate_results::CCornersUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnCandidateQuadEdgesUnitReceived(ddn::intermediate_results::CCandidateQuadEdgesUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnCandidateBarcodeZonesUnitReceived(dbr::intermediate_results::CCandidateBarcodeZonesUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnScaledUpBarcodeImageUnitReceived(dbr::intermediate_results::CScaledUpBarcodeImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnDeformationResistedBarcodeImageUnitReceived(dbr::intermediate_results::CDeformationResistedBarcodeImageUnit *pResult, const IntermediateResultExtraInfo* info);
    virtual void OnComplementedBarcodeImageUnitReceived(dbr::intermediate_results::CComplementedBarcodeImageUnit *pResult, const IntermediateResultExtraInfo* info);
};
```
