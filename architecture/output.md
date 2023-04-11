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

# Standard Output

As the last piece of the Dynamsoft Capture Vision (DCV) architecture, the standard output is responsible for transporting the image processing results to objects that logically depend on them.

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

These results are "final" because they are only returned after an image has finished processing. In other words, for each image, the CRR callback functions are only triggered once when it has finished processing. 

The CRR interface consists of 

1. A callback function that returns all six types of results. This function is always triggered.
2. Six callback functions for each of the six types of results. These functions are only triggered when their corresponding types of results exist.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- Python
   >- Java
   >- C#
   >- C++
   >- C
   >
>
```javascript
interface CapturedResultReceiver {
    /**
     * The callback that contains all results.
     */
    onCapturedResultReceived?: (pResult: Core.BasicStructures.CapturedResult) => void;
    /**
     * The callback that contains only the original raw image.
     */
    onRawImageResultReceived?: (pResult: RawImageResultItem) => void;
    /**
     * The callback that contains all barcode text found on the image.
     */
    onDecodedBarcodesReceived?: (pResult: Core.BasicStructures.CapturedResult) => void;
    /**
     * The callback that contains all text lines found on the image.
     */
    onRecognizedTextLinesReceived?: (pResult: Core.BasicStructures.CapturedResult) => void;
    /**
     * The callback that contains all document boundaries found on the image.
     */
    onDetectedQuadsReceived?: (pResult: Core.BasicStructures.CapturedResult) => void;
    /**
     * The callback that contains all normalized images.
     */
    onNormalizedImagesReceived?: (pResult: Core.BasicStructures.CapturedResult) => void;
    /**
     * The callback that contains data tables parsed from barcode text or text line(s) on the image.
     */
    onParsedResultsReceived?: (pResult: Core.BasicStructures.CapturedResult) => void;
}
```
>```java

```
>```objc

```
>```swift

```
>```python

```
>```java

```
>```csharp

```
>```c++

```
>```c

```


## Intermediate Result Receiver

Intermediate Result Receiver (IRR) is an interface for the output of intermediate results. Intermediate results refer to the following 27 types of results:

1. Predetected regions unit
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

> For the JavaScript Edition, these results are returned at the same time after the image has finished processing.

The IRR interface consists of 27 callback functions for each of the 27 types of results.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- Python
   >- Java
   >- C#
   >- C++
   >- C
   >
>
```javascript
interface IntermediateResultReceiver {
    onPredetectedRegionsReceived?: (targetROIDefName: string,
        taskName: string,
        unit: PredetectedRegionsUnit
    ) => void;

    onLocalizedBarcodesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.LocalizedBarcodesUnit) => void;

    onDecodedBarcodesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.DecodedBarcodesUnit) => void;

    onLocalizedTextLinesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DLR.IntermediateResult.LocalizedTextLinesUnit) => void;

    onRecognizedTextLinesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DLR.IntermediateResult.RecognizedTextLinesUnit) => void;

    onDetectedQuadsReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.DetectedQuadsUnit) => void;

    onNormalizedImagesReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.NormalizedImageUnit) => void;

    onColourImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: ColourImageUnit) => void;

    onScaledDownColourImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: ScaledDownColourImageUnit) => void;

    onGrayscaleImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: GrayscaleImageUnit) => void;

    onTransformedGrayscaleImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TransformedGrayscaleImageUnit) => void;

    onEnhancedGrayscaleImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: EnhancedGrayscaleImageUnit) => void;

    onBinaryImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: BinaryImageUnit) => void;

    onTextureDetectionResultUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextureDetectionResultUnit) => void;

    onTextureRemovedGrayscaleImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextureRemovedGrayscaleImageUnit) => void;

    onTextureRemovedBinaryImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextureRemovedBinaryImageUnit) => void;

    onContoursUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: ContoursUnit) => void;

    onLineSegmentsUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: LineSegmentsUnit) => void;

    onTextZonesUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextZonesUnit) => void;

    onTextRemovedBinaryImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        sectionType: EnumSectionType,
        unit: TextRemovedBinaryImageUnit) => void;

    onLongLinesUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.LongLinesUnit) => void;

    onCornersUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.CornersUnit) => void;

    onCandidateQuadEdgesUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DDN.IntermediateResult.CandidateQuadEdgesUnit) => void;

    onCandidateBarcodeZonesUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.CandidateBarcodeZonesUnit) => void;

    onScaledUpBarcodeImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.ScaledUpBarcodeImageUnit) => void;

    onDeformationResistedBarcodeImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.DeformationResistedBarcodeImageUnit) => void;

    onComplementedBarcodeImageUnitReceived?: (targetROIDefName: string,
        taskName: string,
        unit: DBR.IntermediateResult.ComplementedBarcodeImageUnit) => void;
}
```
>
```java

```
>
```objc

```
>
```swift

```
>
```python

```
>
```java

```
>
```csharp

```
>
```c++

```
>
```c

```