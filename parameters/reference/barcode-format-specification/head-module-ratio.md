---
layout: default-layout
title: HeadModuleRatio - Dynamsoft Barcode Reader Parameters
description: The parameter HeadModuleRatio of Dynamsoft Barcode Reader defines the module count and module size ratio of the barcode head section.
keywords: HeadModuleRatio , parameter reference, parameter
---

# HeadModuleRatio

`HeadModuleRatio` defines the module count and module size ratio of the barcode head section.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── HeadModuleRatio
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "HeadModuleRatio": "211412"
}
```

> [!NOTE]
> - This snippet shows only the `HeadModuleRatio` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `HeadModuleRatio` is shown as follow:

| HeadModuleRatio  Parameter Details |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>N/A |
| **Default Value**<br> "" |

**Remarks**

- The length of the string indicates the count of the barcode head section.
- The number in the string expresses the ratio relationship between the modules.

### Default Settings

If the `HeadModuleRatio` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "HeadModuleRatio": ""
}
```
