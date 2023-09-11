---
layout: default-layout
title: BaseBarcodeReaderTaskSettingName - Dynamsoft Barcode Reader Parameters
description: The parameter BaseBarcodeReaderTaskSettingName of Dynamsoft Barcode Reader defines the name of base BarcodeReaderTaskSetting.
keywords: Base barcode reader task setting name
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/base-barcode-reader-task-setting-name.html
---

#  BaseBarcodeReaderTaskSettingName

Parameter `BaseBarcodeReaderTaskSettingName` represents the name of another `BarcodeReaderTaskSetting` object. It is used to inherit the parameters defined in its parent `BarcodeReaderTaskSetting` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.

## Example

```json
{
    "BaseBarcodeReaderTaskSettingName": "BR_0"
}
```

## Parameter Summary

| BaseBarcodeReaderTaskSettingName Parameter Summary |
| :----------------------------------------- |
| **Type**<br>*String* |
| **Range**<br>One of the existing `BarcodeReaderTaskSetting` object name. |
| **Default Value**<br>"" |
| **Remarks**<br>The default value "" means this object don't inherit the settings of another object. |
