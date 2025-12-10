---
layout: default-layout
title: SectionArray - Dynamsoft Barcode Reader Parameters
description: The parameter SectionArray defines which sections exist under the BarcodeReaderTaskSetting.
keywords: Section Array parameter
---

# SectionArray

Parameter `SectionArray` defines which sections exist under the `BarcodeReaderTaskSetting`. A `Section` is a sequence of `Stages` that form a relatively complete processing unit, producing milestone results that include location information along with other details.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── SectionArray
```

**Parent object:** [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html) object

**Example:**

```json
{
    "SectionArray": [
        {
            "Section": "ST_REGION_PREDETECTION"
        },
        {
            "Section": "ST_BARCODE_LOCALIZATION"
        },
        {
            "Section": "ST_BARCODE_DECODING"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows only the `SectionArray` parameter.
> - To use it, embed this parameter within a [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The `BarcodeReaderTaskSetting` includes the following sections:

* [RegionPredetectionSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-region-predetection.html) (`ST_REGION_PREDETECTION`)
  * Designed to find regions of interest (ROIs) and thus ignore other parts of the image during subsequent processing.
* [BarcodeLocalizationSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-localization.html) (`ST_BARCODE_LOCALIZATION`)
  * Designed to detect the exact locations of barcodes.
* [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html) (`ST_BARCODE_DECODING`)
  * Designed to decode the barcode from the localized barcode areas identified in the previous `BarcodeLocalizationSection` section.
