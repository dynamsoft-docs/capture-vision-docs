---
layout: default-layout
title: Document Detection
description: This is the document detection page of Dynamsoft Capture Vision documents.
keywords: document detetion
needAutoGenerateSidebar: true
breadcrumbText: Document Detection
---

# Section 2.2 - Document Detection

Document detection is one of the key feature of Dynamsoft Document Normalizer (DDN). If DDN tasks are arranged in the settings, the library will try detecting document boundaries from the image and output the location of the detectedd boundaries.

Preprocessing setting are available for DDN module. As a result, the preprocessing intermediate results can be inherited when performing the document detection algorithm.

## Main Work Flow

Based on the binary image output by section 2.1, DDN module performs boundary detection process on the image. It initially find contours of the target items and extract line segments from the contours. After a series of process, the library calculates the corners, edges and finally confirms the locations of the boundaries. Each boundary is output as a quadrilateral with the coordinates of its four vertices.

<div align="center">
   <p><img src="../assets/document-detection.png" alt="document-detection" width="30%" /></p>
   <p></p>
</div>

## Available Intermediate Results

### Document Detection Intermediate Results

| Name | Description |
| ---- | ----------- |
| [`ContoursUnit`] | The detected contours on the image. |
| [`LineSegmentsUnit`] | The line segments extracted from the contours. |
| [`LongLinesUnit`] | Merged from the line segments. |
| [`CornersUnit`] | Formed by intersected long lines. Corners participate in assembling quadrilaterals. |
| [`CandidateQuadEdgesUnit`] | The assembled quadrilaterals. |

### Shared Preprocessing Intermediate Results

| Name | Description | Related Parameter(s) |
| ---- | ----------- | -------------------- |
| `ColourImageUnit` | The colour images. Generally, they are the original images. | N/A |
| `ScaledDownColourImageUnit` | The scaled down colour images. | `ScaleDownThreshold` |
| `GrayscaleImageUnit` | The gray scale images. | `ColourConversionModes` |
| `TransformedGrayscaleImageUnit` | The colour inverted gray scale images. | `GrayscaleTransformationModes` |
| `PredetectedRegionsUnit` | The coordinates of predetected regions quadrilateral(s) | `RegionPredetectionModes` |
| `EnhancedGrayscaleImageUnit` | The enhanced gray scale images. | `ImagePreprocessingModes` |
| `BinaryImageUnit` | The binary images. | `BinarizationModes` |
| `TextureDetectionResultUnit` | The detected texture. | `TextureDetectionModes` |
| `TextureRemovedGrayscaleImageUnit` | The gray scale images that have been removed texture. | `TextureDetectionModes` |
| `TextureRemovedBinaryImageUnit` | The binary images that have been removed texture. | `TextureDetectionModes` |
| `TextRemovedBinaryImageUnit` | The gray scale images that have been removed text. | `TextFilterModes` |
