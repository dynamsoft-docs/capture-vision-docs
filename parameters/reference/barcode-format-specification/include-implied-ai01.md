---
layout: default-layout
title: IncludeImpliedAI01 - Dynamsoft Barcode Reader Parameters
description: The parameter IncludeImpliedAI01 of Dynamsoft Barcode Reader defines whether to prepend the implied "01" at the beginning of the result bytes/text.
keywords: IncludeImpliedAI01, parameter reference, parameter
---

# IncludeImpliedAI01

Parameter `IncludeImpliedAI01` defines whether to prepend the implied "01" at the beginning of the result bytes/text.

## Example

```json
{
    "IncludeImpliedAI01": 1
}
```

## Parameter Summary

The structure of the `IncludeImpliedAI01` is shown as follow:

| IncludeImpliedAI01  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br>0 |

**Remarks**

- 0: exclude.
- 1: include.
- This parameter is valid only for GS1_DATABAR/GS1_COMPOSITE code formats.

**Availability**

Introduced in version 11.0.4000.
