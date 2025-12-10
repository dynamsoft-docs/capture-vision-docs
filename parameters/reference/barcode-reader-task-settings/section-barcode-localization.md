---
layout: default-layout
title: BarcodeLocalizationSection - Dynamsoft Barcode Reader Parameters
description: The BarcodeLocalizationSection defines configuration settings for the barcode localization process.
keywords: BarcodeLocalizationSection
---

# BarcodeLocalizationSection

`BarcodeLocalizationSection` defines the configuration settings for the barcode localization process. In JSON, it is represented as a Section object with `"Section": "ST_BARCODE_LOCALIZATION"`.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── SectionArray[j] (Section object where Section = "ST_BARCODE_LOCALIZATION")
```

**Parent object:** [SectionArray]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-array.html)

**Example:**

```json
{
    "Section": "ST_BARCODE_LOCALIZATION",
    "ImageParameterName": "ip_dbrDefault",
    "StageArray": [
        {
            "Stage": "SST_LOCALIZE_CANDIDATE_BARCODES"
        },
        {
            "Stage": "SST_LOCALIZE_BARCODES"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Section object configured for barcode localization.
> - To use it, add this object to the [SectionArray]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-array.html) of a [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Section

Specifies the section type. Fixed value: `ST_BARCODE_LOCALIZATION`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"ST_BARCODE_LOCALIZATION"` |

### ImageParameterName

Specifies the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object to apply in the stages of this section.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>Must be the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object defined under `ImageParameterOptions` |
| **Default Value**<br>`""` |

### StageArray

Specifies the stage objects within this section. The `BarcodeLocalizationSection` consists of the following stages:

| Stage | Description |
|-------|-------------|
| [LocalizeCandidateBarcodesStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-localize-candidate-barcodes.html) (`SST_LOCALIZE_CANDIDATE_BARCODES`) | Detects and marks potential barcode locations within the image for further processing. |
| [LocalizeBarcodesStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-localize-barcodes.html) (`SST_LOCALIZE_BARCODES`) | Accurately determines the positions of barcodes within the identified candidate regions. |
