---
layout: default-layout
title: Parameters Introduction - Dynamsoft Capture Vision
description: This article introduces Dynamsoft Capture Vision Parameters.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /parameters/index.html
---

# Introduction to Dynamsoft Capture Vision Parameters

[Dynamsoft Capture Vision Architecture](../architecture/index.md) is designed to accommodate both entry-level needs and sophisticated business logic. While [Capture Vision Router](../architecture/index.md#capture-vision-router) allows developers to get started with image-processing in their applications within hours, the Dynamsoft Capture Vision (DCV) parameters are what make it possible for the applications to be able to handle all sorts of image-processing scenarios without changing the code much.

Simply put, DCV parameters are used to configure how different functional products work in the Dynamsoft Capture Vision architecture.

These docs help you learn and use the DCV parameters.

## Parameter File

### File Overview

The following topics are covered in the [Parameter File Overview](file/index.md):

| Topic                                                                                                         | Description                                                                  |
| :------------------------------------------------------------------------------------------------------------ | :--------------------------------------------------------------------------- |
| [Organization of a Parameter Template File](file/index.md#organization-of-a-parameter-template-file).         | A template file contains one or multiple templates.                          |
| [Structure of a Parameter Template](file/index.md#structure-of-a-parameter-template).                         | A template is a predefined configuration of parameters.                      |
| [How to Apply DCV Parameters](file/index.md#how-to-apply-dcv-parameters).                                     | This topic discusses how to interact with DCV to import or update templates. |
| [Special Rules for DCV Parameter Configuration](file/index.md#special-rules-for-dcv-parameter-configuration). | This topic talks about special rules to note when defining templates.        |

### File Component Objects

Each of the objects that make up a Parameter File is introduced in detail:

| Item Name                                                                               | Corresponding Object in a Parameter File |
| :-------------------------------------------------------------------------------------- | :--------------------------------------- |
| [CaptureVisionTemplate](file/capture-vision-template.md).                               | `CaptureVisionTemplates`                 |
| [ImageSource](file/image-source.md).                                                    | `ImageSourceOptions`                     |
| [TargetROIDefinition](file/target-roi-definition/index.md)                             | `TargetROIDefOptions`                    |
| [SemanticProcessingDefinition](file/semantic-processing/index.md)               | `SemanticProcessingOptions`              |
| [BarcodeReaderTaskSetting](file/task-settings/barcode-reader-task-settings.md)           | `BarcodeReaderTaskSettingOptions`        |
| [DocumentNormalizerTaskSetting](file/task-settings/document-normalizer-task-settings.md) | `DocumentNormalizerTaskSettingOptions`   |
| [LabelRecognizerTaskSetting](file/task-settings/label-recognizer-task-settings.md)       | `LabelRecognizerTaskSettingOptions`      |
| [CodeParserTaskSetting](file/task-settings/code-parser-task-settings.md)                 | `CodeParserTaskSettingOptions`           |
| [ImageParameter](file/image-parameter.md)                                               | `ImageParameterOptions`                  |
| [BarcodeFormatSpecification](file/auxiliary/barcode-format-specification.md)            | `BarcodeFormatSpecificationOptions`      |
| [TextLineSpecification](file/auxiliary/textline-specification.md)                       | `TextLineSpecificationOptions`           |
| [CharacterModel](file/auxiliary/character-model.md)                                     | `CharacterModelOptions`                  |
| [GlobalParameter](file/auxiliary/global-parameter.md)                                   | `GlobalParameter`                        |

## Parameter Reference

Parameters that make up the items mentioned in [File Component Objects](#file-component-objects) are explained in details in the reference pages. Check out the [reference index](reference/index.md) for a full list of parameters.