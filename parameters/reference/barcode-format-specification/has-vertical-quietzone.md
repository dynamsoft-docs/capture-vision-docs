---
layout: default-layout
title: HasVerticalQuietZone - Dynamsoft Barcode Reader Parameters
description: The parameter Code128Subset of Dynamsoft Barcode Reader defines whether there is a sufficient vertical quiet zone above and below the barcode.
keywords: HasVerticalQuietZone , parameter reference, parameter
---

# HasVerticalQuietZone

Parameter `HasVerticalQuietZone` defines whether there is a sufficient vertical quiet zone above and below the barcode.

**Remarks**

- Introduced in version 11.2.1000.

## Example

```json
{
    "HasVerticalQuietZone": 0
}
```

## Parameter Summary

The structure of the `HasVerticalQuietZone` is shown as follow:

| HasVerticalQuietZone  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 1] |
| **Default Value**<br> 1|

**Remarks**

- 0: Do not require a sufficient vertical quiet zone above and below the barcode.
- 1: Require a sufficient vertical quiet zone above and below the barcode.
