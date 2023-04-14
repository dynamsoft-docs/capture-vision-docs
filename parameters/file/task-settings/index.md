---
layout: default-layout
title: Dynamsoft Capture Vision Architecture
description: This is the main page of Dynamsoft Capture Vision Architecture. 
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /parameters/file/task-settings/index.html
---

# Task Settings

Each functional product can perform its own individual task. These tasks are configured with the following objects:

| Settings Object                                                                | Task Type                  | Performed By | Category            | Result Type             |
| :----------------------------------------------------------------------------- | :------------------------- | :----------- | :------------------ | :---------------------- |
| [`BarcodeReaderTaskSettingOptions`](barcode-reader-task-settings.md)           | Read Barcodes              | DBR          | Image-Processing    | Decoded Barcodes        |
| [`LabelRecognizerTaskSettingOptions`](label-recognizer-task-settings.md)       | Recognize Text Lines       | DLR          | Image-Processing    | Recognized TextLines    |
| [`DocumentNormalizerTaskSettingOptions`](document-normalizer-task-settings.md) | Detect Document Boundaries | DDN          | Image-Processing    | Document Boundary Quads |
| [`DocumentNormalizerTaskSettingOptions`](document-normalizer-task-settings.md) | Normalize a Document       | DDN          | Image-Processing    | Normalized Image        |
| [`CodeParserTaskSettingOptions`](code-parser-task-settings.md)                 | Parse a string             | DCP          | Semantic-Processing | Parsed Items            |
