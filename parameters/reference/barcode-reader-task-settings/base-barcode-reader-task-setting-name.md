---
layout: default-layout
Title: BaseBarcodeReaderTaskSettingName - Dynamsoft Barcode Reader Parameters
Description: The parameter BaseBarcodeReaderTaskSettingName of Dynamsoft Barcode Reader defines the name of base BarcodeReaderTaskSetting.
Keywords: Base barcode reader task setting name
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/base-barcode-reader-task-setting-name.html
---

#  BaseBarcodeReaderTaskSettingName

Specify a `BarcodeReaderTaskSetting` object name. The current object will inherit the parameter settings of the specified object.

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
