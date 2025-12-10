---
layout: default-layout
title: ReturnBarcodeZoneClarity - Dynamsoft Barcode Reader Parameters
description: The parameter ReturnBarcodeZoneClarity defines whether to return the clarity of the barcode zone.
keywords: Barcode zone clarity
---

# ReturnBarcodeZoneClarity

`ReturnBarcodeZoneClarity` defines whether to return the clarity of the barcode zone.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_DECODE_BARCODES")
            └── ReturnBarcodeZoneClarity
```

**Parent object:** [DecodeBarcodesStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-decode-barcodes.html)

**Example:**

```json
{
    "ReturnBarcodeZoneClarity": 0
}
```

> [!NOTE]
> - This snippet shows only the `ReturnBarcodeZoneClarity` parameter.
> - To use it, embed this parameter within a [DecodeBarcodesStage]({{ site.dcvb_parameters_reference }}barcode-reader-task-settings/stage-decode-barcodes.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| ReturnBarcodeZoneClarity Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: do not return the clarity of the barcode zone.
- 1: return the clarity of the barcode zone.
