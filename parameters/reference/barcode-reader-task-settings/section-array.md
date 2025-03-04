---
layout: default-layout
title: SectionArray - Dynamsoft Barcode Reader Parameters
description: The parameter SectionArray defines which sections exist under the BarcodeReaderTaskSetting.
keywords: Section Array parameter
---

# SectionArray

`SectionArray` is a parameter that defines which sections exist under the `BarcodeReaderTaskSetting`. A `Section` is a sequence of `Stages` that form a relatively complete processing unit, producing milestone results that include location information along with other details.

The `BarcodeReaderTaskSetting` includes the following sections:

* [RegionPredetectionSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-region-predetection.html)
  * It is designed to find regions of interest (ROIs) and thus ignoring other parts of the image during subsequent processing.
* [BarcodeLocalizationSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-localization.html)
  * It is designed to detect the exact locations of barcodes.
* [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html)
  * It is designed to decode the barcode from the locolized barcode areas identified in the previous `BarcodeLocalizationSection` section.

```json
{
    "SectionArray":
    [
        {
            "Section": "ST_REGION_PREDETECTION",
            // Other parameters...
        },
        {
            "Section": "ST_BARCODE_LOCALIZATION",
            // Other parameters...
        },
        {
            "Section": "ST_BARCODE_DECODING",
            // Other parameters...
        }
    ]
}
```
