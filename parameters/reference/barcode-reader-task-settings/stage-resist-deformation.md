---
layout: default-layout
title: ResistDeformationStage - Dynamsoft Barcode Reader Parameters
description: The ResistDeformationStage applies preprocessing to reduce image deformation.
keywords: ResistDeformationStage
---

# ResistDeformationStage

`ResistDeformationStage` applies preprocessing techniques to reduce image deformation and improve barcode recognition accuracy. In JSON, it is represented as a Stage object with `"Stage": "SST_RESIST_DEFORMATION"`.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_RESIST_DEFORMATION")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html#stagearray) within [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html)

**Example:**

```json
{
    "Stage": "SST_RESIST_DEFORMATION",
    "DeformationResistingModes": [
        {
            "Mode": "DRM_SKIP"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for deformation resistance.
> - To use it, add this object to the `StageArray` within a [BarcodeDecodingSection]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/section-barcode-decoding.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_RESIST_DEFORMATION`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_RESIST_DEFORMATION"` |

### DeformationResistingModes

Defines how to handle distorted and deformed barcodes. See [`DeformationResistingModes`]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/deformation-resisting-modes.html) for details. 
