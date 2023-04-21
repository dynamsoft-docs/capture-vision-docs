---
layout: default-layout
Title: HeadModuleRatio - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for HeadModuleRatio.
Keywords: HeadModuleRatio , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/head-module-ratio.html
---

# HeadModuleRatio  

`HeadModuleRatio` defines the module count and module size ratio of the barcode head section.
## Example


```json
{
    "HeadModuleRatio": "211412"
}
```

## Parameter Summary
The structure of the`HeadModuleRatio` is shown as follow:

| HeadModuleRatio  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>N/A |
| **Default Value**<br> ""|

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