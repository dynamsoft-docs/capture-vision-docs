---
layout: default-layout
title: BarcodeDecodingSection - Dynamsoft Barcode Reader Parameters
description: The BarcodeDecodingSection defines configuration settings for the barcode decoding process.
keywords: BarcodeDecodingSection
---

# BarcodeDecodingSection

`BarcodeDecodingSection` defines the configuration settings for the barcode decoding process. In JSON, it is represented as a Section object with `"Section": "ST_BARCODE_DECODING"`.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── SectionArray[j] (Section object where Section = "ST_BARCODE_DECODING")
```

**Parent object:** [SectionArray]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-array.html)

**Example:**

```json
{
    "Section": "ST_BARCODE_DECODING",
    "ImageParameterName": "ip_dbrDefault",
    "StageArray": [
        {
            "Stage": "SST_RESIST_DEFORMATION"
        },
        {
            "Stage": "SST_DECODE_BARCODES"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Section object configured for barcode decoding.
> - To use it, add this object to the [SectionArray]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-array.html) of a [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Section

Specifies the section type. Fixed value: `ST_BARCODE_DECODING`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"ST_BARCODE_DECODING"` |

### ImageParameterName

Specifies the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object to apply in the stages of this section.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>Must be the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object defined under `ImageParameterOptions` |
| **Default Value**<br>`""` |

### StageArray

Specifies the stage objects within this section. The `BarcodeDecodingSection` consists of the following stages:

| Stage | Description |
|-------|-------------|
| [ResistDeformationStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-resist-deformation.html) (`SST_RESIST_DEFORMATION`) | Applies preprocessing techniques to reduce image deformation and improve barcode recognition accuracy. |
| [ComplementBarcodeStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-complement-barcode.html) (`SST_COMPLEMENT_BARCODE`) | Defines configuration settings for the barcode complement process. |
| [ScaleBarcodeImageStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-scale-barcode-image.html) (`SST_SCALE_BARCODE_IMAGE`) | Scales the barcode image according to the specified scaling mode to optimize recognition. |
| [DecodeBarcodesStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-decode-barcodes.html) (`SST_DECODE_BARCODES`) | Extracts and interprets barcode data from the localized barcode regions. |
