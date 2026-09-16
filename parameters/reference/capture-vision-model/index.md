---
layout: default-layout
title: CaptureVisionModel Parameters - Dynamsoft Capture Vision
description: Reference index for CaptureVisionModel object in Dynamsoft Capture Vision parameters, which defines how the library finds CNN model files and how to configure model arguments such as CharSet.
keywords: CaptureVisionModel, CharSet, model, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# CaptureVisionModel Parameters

The `CaptureVisionModel` object defines how the library finds Convolutional Neural Networks (CNN) model files that support barcode decoding, character recognition and text line recognition.

## Supported CNN Model Files

The following model files are currently supported.

- `Code128Decoder.data`
- `Code39ITFDecoder.data`
- `DataMatrixQRCodeDeblur.data`
- `DataMatrixQRCodeLocalization.data`
- `EAN13Decoder.data`
- `LetterCharRecognition.data`
- `LowercaseCharRecognition.data`
- `MRZCharRecognition.data`
- `MRZLocalization.data`
- `MRZTextLineRecognition.data`
- `NumberCharRecognition.data`
- `NumberLetterCharRecognition.data`
- `NumberLowercaseCharRecognition.data`
- `NumberUppercaseCharRecognition.data`
- `OneDDeblur.data`
- `OneDLocalization.data`
- `PDF417Deblur.data`
- `PDF417Localization.data`
- `TextLineOrientationCls.data`
- `UppercaseCharRecognition.data`
- `VINCharRecognition.data`

## Example JSON

```json
{
    "CaptureVisionModelOptions": [
        {
            "Name": "NumberLetterCharRecognition",
            "DirectoryPath": "D:\\CaptureVisionModel\\",
            "MaxModelInstances": 1,
            "ModelArgs": {
                "CharSet": {
                    "AddSpecialChars": ["-", ":"],
                    "ExcludeChars": ["O", "Q"]
                }
            }
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `CaptureVisionModel` object inside `CaptureVisionModelOptions`.

```text
CaptureVisionModel
├── Name
├── DirectoryPath
├── MaxModelInstances
└── ModelArgs
  └── CharSet
    ├── AddSpecialChars
    └── ExcludeChars
```

## Top-Level Parameters

### Name

The name of the `CaptureVisionModel` object. It will be used as a unique identifier for the model.

| Parameter Summary |
| :------------------- |
| **Type**<br>*String* |
| **Remarks**<br>It must be the filename of the model file. For example, to use the `NumberLetterCharRecognition.data` model file, you need to set `Name` to "NumberLetterCharRecognition". |

### DirectoryPath

The directory path of the model file.

| Parameter Summary |
| :------------------- |
| **Type**<br>*String* |
| **Default Value**<br>"" |

### MaxModelInstances

The maximum number of instances of the model.

| Parameter Summary |
| :------------------- |
| **Type**<br>*int* |
| **Range**<br>[1,256] |
| **Default Value**<br>1 (4 for single character model) |


### ModelArgs

Sets advanced arguments of the model.

| Parameter Summary |
| :------------------- |
| **Type**<br>*JSON object* |
| **Remarks**<br>Currently, [CharSet](char-set.md) is supported |

## Nested Parameter Quick Links

### Actual Nested Parameters in the Tree

| Parameter Name | Description |
|:---------------|:------------|
| [`CharSet`](char-set.md) | Defines the character recognition scope for the model by adding special characters and excluding unwanted characters. |
