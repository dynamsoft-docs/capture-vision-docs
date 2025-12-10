---
layout: default-layout
title: TailModuleRatio - Dynamsoft Barcode Reader Parameters
description: The parameter TailModuleRatio of Dynamsoft Barcode Reader defines the module count and module size ratio of the barcode tail section.
keywords: TailModuleRatio , parameter reference, parameter
---

# TailModuleRatio

`TailModuleRatio` defines the module count and module size ratio of the barcode tail section.
## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── TailModuleRatio
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "TailModuleRatio": "233112"
}
```

> [!NOTE]
> - This snippet shows only the `TailModuleRatio` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the`TailModuleRatio` is shown as follow:

| TailModuleRatio  Parameter Details |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>N/A |
| **Default Value**<br>"" |

**Remarks**

- The length of the string indicates the count of the barcode tail section.
- The number in the string expresses the ratio relationship between the modules.
