---
layout: default-layout
title: DeblurLevel - Dynamsoft Barcode Reader Parameters
description: The parameter DeblurLevel of Dynamsoft Barcode Reader defines the efforts used to process the blurriness of the barcode.
keywords: Base barcode reader task setting name
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/deblur-level.html
---

# DeblurLevel

Parameter `DeblurLevel` defines the efforts used to process the blurriness of the barcode.

## Example

```json
{
    "DeblurLevel" : 9
}
```

## Parameter Summary

| DeblurLevel Parameter Summary |
| :----------------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0,9] |
| **Default Value**<br>9 |

## DeblurLevel VS DeblurModes

`DeblurLevel` is a simplied setting of `DeblurModes`. The following tables shows the relationship between `DeblurLevel` and `DeblurModes`:

### For PDF417 Barcodes

| DeblurLevel | DeblurModes |
| :---------- | :---------- |
| 0 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION] |
| 1-3 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION] |
| 4-6 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_SMOOTHING] |
| 7-8 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_SMOOTHING,DM_GRAY_EQUALIZATION] |
| 9 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_SMOOTHING,DM_GRAY_EQUALIZATION,DM_MORPHING,DM_DEEP_ANALYSIS] |

### For OneD Barcodes

| DeblurLevel | DeblurModes |
| :---------- | :---------- |
| 0 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_THRESHOLD_BINARIZATION] |
| 1-3 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION] |
| 4-6 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_SMOOTHING] |
| 7-8 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_SMOOTHING,DM_GRAY_EQUALIZATION] |
| 9 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_DEEP_ANALYSIS,DM_SMOOTHING,DM_GRAY_EQUALIZATION,DM_MORPHING] |

### For Other Barcodes

| DeblurLevel | DeblurModes |
| :---------- | :---------- |
| 0 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION] |
| 1-3 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION] |
| 4-6 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_SMOOTHING] |
| 7-8 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_SMOOTHING,DM_GRAY_EQUALIZATION] |
| 9 | [DM_BASED_ON_LOC_BIN,DM_THRESHOLD_BINARIZATION,DM_DIRECT_BINARIZATION,DM_DEEP_ANALYSIS,DM_SMOOTHING,DM_GRAY_EQUALIZATION,DM_MORPHING] |
