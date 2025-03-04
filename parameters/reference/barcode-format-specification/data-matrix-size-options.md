---
layout: default-layout
title: DataMatrixSizeOptions - Dynamsoft Barcode Reader Parameters
description: The parameter DataMatrixSizeOptions of Dynamsoft Barcode Reader defines expected size of the DataMatrix to be decoded.
keywords: DataMatrixSizeOptions, parameter reference, parameter
---

# DataMatrixSizeOptions

Parameter `DataMatrixSizeOptions` defines expected size of the DataMatrix to be decoded.

## Example

```json
{
    "DataMatrixSizeOptions": ["DMS_DEFAULT"]
}
```

## Parameter Summary

The structure of the `DataMatrixSizeOptions` is shown as follow:

| DataMatrixSizeOptions  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string[]* |
| **Range**<br>["DMS_DEFAULT","DMS_ALL","DMS_SQUARE","DMS_RECTANGLE","DMS_DMRE","DMS_SQUARE_10_10","DMS_SQUARE_12_12","DMS_SQUARE_14_14","DMS_SQUARE_16_16","DMS_SQUARE_18_18","DMS_SQUARE_20_20","DMS_SQUARE_22_22","DMS_SQUARE_24_24","DMS_SQUARE_26_26","DMS_SQUARE_32_32","DMS_SQUARE_36_36","DMS_SQUARE_40_40","DMS_SQUARE_44_44","DMS_SQUARE_48_48","DMS_SQUARE_52_52","DMS_SQUARE_64_64","DMS_SQUARE_72_72","DMS_SQUARE_80_80","DMS_SQUARE_88_88","DMS_SQUARE_96_96","DMS_SQUARE_104_104","DMS_SQUARE_120_120","DMS_SQUARE_132_132","DMS_SQUARE_144_144","DMS_RECTANGLE_8_18","DMS_RECTANGLE_8_32","DMS_RECTANGLE_12_26","DMS_RECTANGLE_12_36","DMS_RECTANGLE_16_36","DMS_RECTANGLE_16_48","DMS_DMRE_8_48","DMS_DMRE_8_64","DMS_DMRE_8_80","DMS_DMRE_8_96","DMS_DMRE_8_120","DMS_DMRE_8_144","DMS_DMRE_12_64","DMS_DMRE_12_88","DMS_DMRE_16_64","DMS_DMRE_20_36","DMS_DMRE_20_44","DMS_DMRE_20_64","DMS_DMRE_22_48","DMS_DMRE_24_48","DMS_DMRE_24_64","DMS_DMRE_26_40","DMS_DMRE_26_48","DMS_DMRE_26_64"] |
| **Default Value**<br> ["DMS_DEFAULT"] |

**Remarks**

- It is valid only for DataMatrix.
- DMS_DEFAULT: A combination of DMS_SQUARE, DMS_RECTANGLE, and the following specific DMRE sizes: "DMS_DMRE_16_64","DMS_DMRE_20_36","DMS_DMRE_20_44","DMS_DMRE_20_64","DMS_DMRE_22_48","DMS_DMRE_24_48","DMS_DMRE_24_64","DMS_DMRE_26_40","DMS_DMRE_26_48","DMS_DMRE_26_64".
- DMS_ALL: A combination of all available size options, including square, rectangular, and DMRE sizes.
- DMS_SQUARE: A combination of all square size options (e.g., DMS_SQUARE_10_10, DMS_SQUARE_12_12, etc.).
- DMS_RECTANGLE: A combination of all rectangular size options (e.g., DMS_RECTANGLE_8_18, DMS_RECTANGLE_12_26, etc.).
- DMS_DMRE: A combination of all Data Matrix Rectangular Extension (DMRE) size options (e.g., DMS_DMRE_8_48, DMS_DMRE_20_64, etc.).
