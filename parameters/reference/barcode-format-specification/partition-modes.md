---
layout: default-layout
title: PartitionModes - Dynamsoft Barcode Reader Parameters
description: The parameter PartitionModes of Dynamsoft Barcode Reader is used to select the mode used to apply partition process when decoding QRCode and DataMatrix.
keywords: PartitionModes , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/partition-modes.html
---

# PartitionModes

Parameter `PartitionModes` is used to select the mode used to apply partition process when decoding QRCode and DataMatrix.

## Example

```json
{
    "PartitionModes": ["PM_WHOLE_BARCODE"]
}
```

## Parameter Summary

The structure of the `PartitionModes` is shown as follow:

| PartitionModes  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string array* |
| **Candidate Mode List**<br>PM_WHOLE_BARCODE<br>PM_ALIGNMENT_PARTITION |
| **Default Value**<br> ["PM_WHOLE_BARCODE","PM_ALIGNMENT_PARTITION"] |

## Candidate Mode introduction

### PM_WHOLE_BARCODE

ake the whole barcode for decoding.

### PM_ALIGNMENT_PARTITION

Partition the barcode to blocks based on alignment.
