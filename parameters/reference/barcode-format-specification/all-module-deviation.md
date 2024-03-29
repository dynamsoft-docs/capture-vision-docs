---
layout: default-layout
title: AllModuleDeviation - Dynamsoft Barcode Reader Parameters
description: The parameter AllModuleDeviation of Dynamsoft Barcode Reader specifies the width deviation value (in moduleSize) of a non-standard 1D barcode type relative to the standard barcode width.
keywords: AllModuleDeviation, parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/all-module-deviation.html
---

# AllModuleDeviation

Parameter `AllModuleDeviation` specifies the width deviation value (in moduleSize) of a non-standard 1D barcode type relative to the standard barcode width.

## Example

```json
{
    "AllModuleDeviation": 1
}
```

## Parameter Summary

The unit defined in Parameter `AllModuleDeviation` is barcode module size. For example, if the standard barcode module size is 2px and `AllModuleDeviation` is 1, then the non-standard barcode module size is 4px. The structure of the `AllModuleDeviation` is shown as follow:

| AllModuleDeviation Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br>0 |
