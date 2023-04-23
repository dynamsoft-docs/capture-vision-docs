---
layout: default-layout
Title: RequireStartStopChars - Dynamsoft Barcode Reader Parameters
Description: The parameter RequireStartStopChars of Dynamsoft Barcode Reader defines whether the start and stop characters are required when searching for common 1D barcodes.
Keywords: RequireStartStopChars , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/require-start-stop-chars.html
---

# RequireStartStopChars

Parameter `RequireStartStopChars` defines whether the start and stop characters are required when searching for common 1D barcodes.

## Example

```json
{
    "RequireStartStopChars": 0
}
```

## Parameter Summary

The structure of the`RequireStartStopChars` is shown as follow:

| RequireStartStopChars  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br> 1 |

**Remarks**

- 0: start and stop characters are not required.
- 1: start and stop characters are required.
