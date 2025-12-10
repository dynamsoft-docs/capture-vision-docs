---
layout: default-layout
title: PartitionModes - Dynamsoft Barcode Reader Parameters
description: The parameter PartitionModes of Dynamsoft Barcode Reader is used to select the mode used to apply partition process when decoding QRCode and DataMatrix.
keywords: PartitionModes , parameter reference, parameter
---

# PartitionModes

Parameter `PartitionModes` is used to select the mode used to apply partition process when decoding QRCode and DataMatrix.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── PartitionModes
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "PartitionModes": ["PM_WHOLE_BARCODE"]
}
```

> [!NOTE]
> - This snippet shows only the `PartitionModes` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `PartitionModes` is shown as follow:

| PartitionModes  Parameter Details |
| :--------------------------------- |
| **Type**<br>*string array* |
| **Candidate Mode List**<br>PM_WHOLE_BARCODE<br>PM_ALIGNMENT_PARTITION |
| **Default Value**<br> ["PM_WHOLE_BARCODE","PM_ALIGNMENT_PARTITION"] |

## Candidate Mode introduction

### PM_WHOLE_BARCODE

Take the whole barcode for decoding.

### PM_ALIGNMENT_PARTITION

Partition the barcode to blocks based on alignment.
