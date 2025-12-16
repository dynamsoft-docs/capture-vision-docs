---
layout: default-layout
title: ScaleBarcodeImageStage - Dynamsoft Barcode Reader Parameters
description: The ScaleBarcodeImageStage scales barcode images to optimize recognition.
keywords: ScaleBarcodeImageStage
---

# ScaleBarcodeImageStage

`ScaleBarcodeImageStage` scales barcode images according to the specified scaling mode to optimize recognition. In JSON, it is represented as a Stage object with `"Stage": "SST_SCALE_BARCODE_IMAGE"`.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_SCALE_BARCODE_IMAGE")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html#stagearray) within [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html)

**Example:**

```json
{
    "Stage": "SST_SCALE_BARCODE_IMAGE",
    "BarcodeScaleModes": [
        {
            "Mode": "BSM_AUTO"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for barcode image scaling.
> - To use it, add this object to the `StageArray` within a [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_SCALE_BARCODE_IMAGE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_SCALE_BARCODE_IMAGE"` |

### BarcodeScaleModes

Defines the scaling mode applied during barcode recognition. See [`BarcodeScaleModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/barcode-scale-modes.html) for details. 
