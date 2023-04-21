---
layout: default-layout
Title: MinResultConfidence - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for MinResultConfidence.
Keywords: MinResultConfidence , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/min-result-confidence.html
---

# MinResultConfidence  

`MinResultConfidence` defines the minimum confidence of the result.
## Example


```json
{
    "MinResultConfidence": 20
}
```

## Parameter Summary
The structure of the`MinResultConfidence` is shown as follow:

| MinResultConfidence  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 100] |
| **Default Value**<br> 30|


### Default Settings

If the `MinResultConfidence` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "MinResultConfidence": 30
}
```