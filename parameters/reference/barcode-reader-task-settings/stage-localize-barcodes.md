---
layout: default-layout
title: LocalizeBarcodesStage - Dynamsoft Barcode Reader Parameters
description: The LocalizeBarcodesStage accurately determines the positions of barcodes within the identified candidate regions.
keywords: LocalizeBarcodesStage
---

# LocalizeBarcodesStage

`LocalizeBarcodesStage` accurately determines the positions of barcodes within the identified candidate regions. In JSON, it is represented as a Stage object with `"Stage": "SST_LOCALIZE_BARCODES"`.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_LOCALIZE_BARCODES")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-localization.html#stagearray) within [BarcodeLocalizationSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-localization.html)

**Example:**

```json
{
    "Stage": "SST_LOCALIZE_BARCODES"
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for localizing barcodes.
> - To use it, add this object to the `StageArray` within a [BarcodeLocalizationSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-localization.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_LOCALIZE_BARCODES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_LOCALIZE_BARCODES"` |
