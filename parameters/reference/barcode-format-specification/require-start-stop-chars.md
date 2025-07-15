---
layout: default-layout
title: RequireStartStopChars - Dynamsoft Barcode Reader Parameters
description: The parameter RequireStartStopChars of Dynamsoft Barcode Reader defines whether the start and/or stop characters are required when searching for common 1D barcodes.
keywords: RequireStartStopChars , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/require-start-stop-chars.html
---

# RequireStartStopChars

Parameter `RequireStartStopChars` defines whether the start and/or stop characters are required when searching for common 1D barcodes.

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

- 0: start and/or stop characters are not required.
  >[!NOTE]
  > **Behavior changed in v11.0.4000**: In previous versions, this meant both start and stop characters were not required. Since v11.0.4000, it allows either or both to be missing.
- 1: start and stop characters are required.
