---
layout: default-layout
title: DataMatrixModuleIsotropic - Dynamsoft Barcode Reader Parameters
description: The parameter DataMatrixModuleIsotropic specifies whether the Data Matrix modules are isotropic, meaning they have equal scaling in all directions.
keywords: DataMatrixModuleIsotropic, parameter reference, parameter
---

# DataMatrixModuleIsotropic

Parameter `DataMatrixModuleIsotropic` specifies whether the Data Matrix modules are isotropic, meaning they have equal scaling in all directions.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── DataMatrixModuleIsotropic
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "DataMatrixModuleIsotropic": 1
}
```

> [!NOTE]
> - This snippet shows only the `DataMatrixModuleIsotropic` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `DataMatrixModuleIsotropic` is shown as follow:

| DataMatrixModuleIsotropic  Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- It is valid only for DataMatrix.
- 0: Modules are not required to be isotropic.
- 1: Modules must be isotropic (equal scaling in all directions).
