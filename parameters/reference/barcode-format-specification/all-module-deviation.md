---
layout: default-layout
Title: AllModuleDeviation - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for AllModuleDeviation.
Keywords: AllModuleDeviation, parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/all-module-deviation.html
---

# AllModuleDeviation

`AllModuleDeviation` specifies the width deviation value (in moduleSize) of a non-standard 1D barcode type relative to the standard barcode width.
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

### Default Settings

If the `AllModuleDeviation` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "AllModuleDeviation": 0
}
```
