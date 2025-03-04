---
layout: default-layout
title: DataMatrixModuleIsotropic - Dynamsoft Barcode Reader Parameters
description: The parameter DataMatrixModuleIsotropic specifies whether the Data Matrix modules are isotropic, meaning they have equal scaling in all directions.
keywords: DataMatrixModuleIsotropic, parameter reference, parameter
---

# DataMatrixModuleIsotropic

Parameter `DataMatrixModuleIsotropic` specifies whether the Data Matrix modules are isotropic, meaning they have equal scaling in all directions.

## Example

```json
{
    "DataMatrixModuleIsotropic": 1
}
```

## Parameter Summary

The structure of the `DataMatrixModuleIsotropic` is shown as follow:

| DataMatrixModuleIsotropic  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- It is valid only for DataMatrix.
- 0: Modules are not required to be isotropic.
- 1: Modules must be isotropic (equal scaling in all directions).
