---
layout: default-layout
title: ComplementBarcodeStage - Dynamsoft Barcode Reader Parameters
description: The ComplementBarcodeStage complements missing parts of a barcode.
keywords: ComplementBarcodeStage
---

# ComplementBarcodeStage

`ComplementBarcodeStage` complements missing parts of a barcode. In JSON, it is represented as a Stage object with `"Stage": "SST_COMPLEMENT_BARCODE"`.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_COMPLEMENT_BARCODE")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html#stagearray) within [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html)

**Example:**

```json
{
    "Stage": "SST_COMPLEMENT_BARCODE",
    "BarcodeComplementModes": [
        {
            "Mode": "BCM_SKIP"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for barcode complement.
> - To use it, add this object to the `StageArray` within a [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_COMPLEMENT_BARCODE`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_COMPLEMENT_BARCODE"` |

### BarcodeComplementModes

Defines how to complement the missing parts of a barcode. See [`BarcodeComplementModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/barcode-complement-modes.html) for details. 
