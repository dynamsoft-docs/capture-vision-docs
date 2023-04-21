---
layout: default-layout
Title: TailModuleRatio - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for TailModuleRatio.
Keywords: TailModuleRatio , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/tail-module-ratio.html
---

# TailModuleRatio  

`TailModuleRatio` defines the module count and module size ratio of the barcode tail section.
## Example


```json
{
    "TailModuleRatio": "233112"
}
```

## Parameter Summary
The structure of the`TailModuleRatio` is shown as follow:

| TailModuleRatio  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>N/A |
| **Default Value**<br> ""|

**Remarks**
- The length of the string indicates the count of the barcode tail section.
- The number in the string expresses the ratio relationship between the modules.

### Default Settings

If the `TailModuleRatio` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "TailModuleRatio": ""
}
```