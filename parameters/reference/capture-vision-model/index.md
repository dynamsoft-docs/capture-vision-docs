---
layout: default-layout
title: CaptureVisionModelOptions Parameter Details - Dynamsoft Capture Vision Parameters
description: Details of several CaptureVisionModelOptions parameters in Dynamsoft Capture Vision.
keywords: CaptureVisionModelOptions, model
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# CaptureVisionModelOptions Parameters

## Name

The name of the CaptureVisionModel object. It will be used as a unique identifier for the model.

| Parameter Summary |
| :------------------- |
| **Type**<br>*String* |
| **Remarks**<br>It must be the filename of the model file. For example, to use the `NumberLetterCharRecognition.data` model file, you need to set `Name` to "NumberLetterCharRecognition". |

## DirectoryPath

The directory path of the model file.

| Parameter Summary |
| :------------------- |
| **Type**<br>*String* |
| **Default Value**<br>"" |

## MaxModelInstances

The maximum number of instances of the model.

| Parameter Summary |
| :------------------- |
| **Type**<br>*int* |
| **Range**<br>[1,256] |
| **Default Value**<br>1 (4 for single character model) |

