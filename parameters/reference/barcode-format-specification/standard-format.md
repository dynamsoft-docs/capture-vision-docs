---
layout: default-layout
Title: StandardFormat - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for StandardFormat.
Keywords: StandardFormat , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/standard-format.html
---

# StandardFormat  

`StandardFormat` defines the standard barcode format.
## Example


```json
{
    "StandardFormat": "BF_CODE128"
}
```

## Parameter Summary
The structure of the`StandardFormat` is shown as follow:

| StandardFormat  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>[BarcodeFormat]({{ site.enumerations }}barcode-reader/barcode-format.html#barcodeformat) |
| **Default Value**<br> ""|


### Default Settings

If the `StandardFormat` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "StandardFormat": ""
}
```