---
layout: default-layout
title: BaseBarcodeReaderTaskSettingName - Dynamsoft Barcode Reader Parameters
description: The parameter BaseBarcodeReaderTaskSettingName defines the name of base BarcodeReaderTaskSetting.
keywords: Base barcode reader task setting name
---

# BaseBarcodeReaderTaskSettingName

`BaseBarcodeReaderTaskSettingName` represents the name of another `BarcodeReaderTaskSetting` object. It is used to inherit the parameters defined in its parent `BarcodeReaderTaskSetting` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── BaseBarcodeReaderTaskSettingName
```

**Parent object:** [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html)

**Example:**

```json
{
    "BaseBarcodeReaderTaskSettingName": "BR_0"
}
```

> [!NOTE]
> - This snippet shows only the `BaseBarcodeReaderTaskSettingName` parameter.
> - To use it, embed this parameter within a [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| BaseBarcodeReaderTaskSettingName Parameter Details |
| :----------------------------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the existing `BarcodeReaderTaskSetting` object name. |
| **Default Value**<br>"" |
| **Remarks**<br>The default value "" means this object don't inherit the settings of another object. |
