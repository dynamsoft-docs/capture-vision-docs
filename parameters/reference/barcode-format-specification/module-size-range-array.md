---
layout: default-layout
Title: ModuleSizeRangeArray - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for ModuleSizeRangeArray.
Keywords: ModuleSizeRangeArray , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/module-size-range-array.html
---

# ModuleSizeRangeArray  

`ModuleSizeRangeArray` defines the range of module size (in pixels) while barcode searching and result filtering.
## Example


```json
{
    "ModuleSizeRangeArray": [
    {
        "MinValue": 3,
        "MaxValue": 20
    }
    ]
}
```

## Parameter Summary
`ModuleSizeRangeArray` is not set by default which means there is no limitation on the barcode module size. The structure of the `ModuleSizeRangeArray` is shown as follow:

| ModuleSizeRangeArray  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*A JSON Object array: <br>defines MinValue and MaxValue of the barcode module size.* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br> ""|


### Default Settings

If the `ModuleSizeRangeArray` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "ModuleSizeRangeArray": []
}
```