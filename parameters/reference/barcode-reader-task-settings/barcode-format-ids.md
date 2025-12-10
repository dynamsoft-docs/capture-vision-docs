---
layout: default-layout
title: BarcodeFormatIds - Dynamsoft Barcode Reader Parameters
description: The parameter BarcodeFormatIds defines the barcode formats to read in a task.
keywords: Barcode format IDs
---

# BarcodeFormatIds

`BarcodeFormatIds` defines which barcode formats to read in a barcode reader task. You can specify multiple barcode formats at one time.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── BarcodeFormatIds
```

**Parent object:** [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html)

**Example:**

```json
{
    "BarcodeFormatIds": ["BF_ONED", "BF_DATAMATRIX"]
}
```

> [!NOTE]
> - This snippet shows only the `BarcodeFormatIds` parameter.
> - To use it, embed this parameter within a [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| BarcodeFormatIds Parameter Details |
| :--------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each array element should be a string value from the [BarcodeFormat]({{ site.dcvb_enums }}barcode-reader/barcode-format.html) enumeration. |
| **Default Value**<br>`["BF_DEFAULT"]` |
| **Remarks**<br>View the [BarcodeFormat enumeration]({{ site.dcvb_enums }}barcode-reader/barcode-format.html) for all supported barcode formats. |
