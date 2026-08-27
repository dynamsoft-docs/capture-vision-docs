---
layout: default-layout
title: DocumentNormalizerTaskSetting Parameters - Dynamsoft Capture Vision
description: Reference index for DocumentNormalizerTaskSetting parameters in Dynamsoft Capture Vision, including document detection, deskewing, image enhancement, and normalization settings.
keywords: DocumentNormalizerTaskSetting, document normalizer, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# DocumentNormalizerTaskSetting Parameters

The `DocumentNormalizerTaskSetting` object configures the settings for document detection and normalization in Dynamsoft Capture Vision.

## General

| Parameter | Description |
|:----------|:------------|
| [`Name`](name.html) | The unique name of the DocumentNormalizerTaskSetting object. |
| [`BaseDocumentNormalizerTaskSettingName`](base-document-normalizer-task-setting-name.html) | The name of another DocumentNormalizerTaskSetting to inherit from. |
| [`MaxThreadsInOneTask`](max-threads-in-one-task.html) | The maximum threads in one task. |
| [`ExpectedDocumentsCount`](expected-documents-count.html) | The expected number of documents to detect. |

## Document Properties

| Parameter | Description |
|:----------|:------------|
| [`ContentType`](content-type.html) | The content type of the document. |
| [`ColourMode`](colour-mode.html) | The colour mode for the normalized image. |
| [`Brightness`](brightness.html) | The brightness of the normalized image. |
| [`Contrast`](contrast.html) | The contrast of the normalized image. |
| [`PageSize`](page-size.html) | The page size for normalization. |
| [`CornerAngleRange`](corner-angle-range.html) | The acceptable corner angle range for document detection. |
| [`DeskewMode`](deskew-mode.html) | The mode for deskewing the document. |

## Detection Modes

| Parameter | Description |
|:----------|:------------|
| [`QuadrilateralDetectionModes`](quadrilateral-detection-modes.html) | The modes for detecting document quadrilaterals. |

## Section & Stage Configuration

| Parameter | Description |
|:----------|:------------|
| [`SectionArray`](section-array.html) | The sections of the document normalizer task. |
| [`SectionRegionsPredetection`](section-regions-predetection.html) | Region predetection section settings. |
| [`SectionDocumentDetection`](section-document-detection.html) | Document detection section settings. |
| [`SectionDocumentDeskewing`](section-document-deskewing.html) | Document deskewing section settings. |
| [`SectionImageEnhancement`](section-image-enhancement.html) | Image enhancement section settings. |
| [`StagePredetectRegions`](stage-predetect-regions.html) | Stage for predetecting regions. |
| [`StageDetectCorners`](stage-detect-corners.html) | Stage for detecting corners. |
| [`StageDetectEdges`](stage-detect-edges.html) | Stage for detecting edges. |
| [`StageDetectQuads`](stage-detect-quads.html) | Stage for detecting quadrilaterals. |
| [`StageAssembleLongLines`](stage-assemble-long-lines.html) | Stage for assembling long lines. |
| [`StageAssembleLogicalLines`](stage-assemble-logical-lines.html) | Stage for assembling logical lines. |
| [`StageDeskewImage`](stage-deskew-image.html) | Stage for deskewing the image. |
| [`StageEnhanceImage`](stage-enhance-image.html) | Stage for enhancing the image. |
