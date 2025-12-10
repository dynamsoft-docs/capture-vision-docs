---
layout: default-layout
title: BarcodeFormatSpecificationNameArray - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeFormatSpecificationNameArray defines the collection of BarcodeFormatSpecification object names.
keywords: BarcodeFormatSpecification, BarcodeReaderTaskSetting
---

# BarcodeFormatSpecificationNameArray

`BarcodeFormatSpecificationNameArray` defines the collection of BarcodeFormatSpecification object names, used to refer to the `BarcodeFormatSpecification` objects.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── BarcodeFormatSpecificationNameArray
```

**Parent object:** [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html)

**Example:**

```json
{
    "BarcodeFormatSpecificationNameArray": ["bfs_default"]
}
```

> [!NOTE]
> - This snippet shows only the `BarcodeFormatSpecificationNameArray` parameter.
> - To use it, embed this parameter within a [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| BarcodeFormatSpecificationNameArray Parameter Details |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element is the name of a `BarcodeFormatSpecification` object. |
| **Default Value**<br>null |
| **Remarks**<br>If `BarcodeFormatSpecificationNameArray` is not specified or null, a default configuration will be applied.|
