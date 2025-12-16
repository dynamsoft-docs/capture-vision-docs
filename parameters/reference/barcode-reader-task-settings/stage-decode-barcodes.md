---
layout: default-layout
title: DecodeBarcodesStage - Dynamsoft Barcode Reader Parameters
description: The DecodeBarcodesStage extracts and interprets barcode data from localized barcode regions.
keywords: DecodeBarcodesStage
---

# DecodeBarcodesStage

`DecodeBarcodesStage` extracts and interprets barcode data from localized barcode regions. In JSON, it is represented as a Stage object with `"Stage": "SST_DECODE_BARCODES"`.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_DECODE_BARCODES")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html#stagearray) within [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html)

**Example:**

```json
{
    "Stage": "SST_DECODE_BARCODES",
    "DeblurModes": [
        {
            "Mode": "DM_DIRECT_BINARIZATION"
        }
    ],
    "ReturnBarcodeZoneClarity": 0
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for barcode decoding.
> - To use it, add this object to the `StageArray` within a [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_DECODE_BARCODES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_DECODE_BARCODES"` |

### DeblurModes

Defines the mode and priority for deblurring. See [`DeblurModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deblur-modes.html) for details.

### ReturnBarcodeZoneClarity

Specifies whether to return the clarity of the barcode zone. See [`ReturnBarcodeZoneClarity`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/return-barcode-zone-clarity.html) for details. 
