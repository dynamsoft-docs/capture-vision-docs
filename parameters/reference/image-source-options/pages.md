---
layout: default-layout
title: Pages - Dynamsoft Capture Vision Parameters
description: The parameter Pages of Dynamsoft Capture Vision defines .
keywords: Pages, ISA
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Pages

Parameter `Pages` sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching.

## Example

```json
{
    "Pages": [0,3,5,7,10]
}
```

## Parameter Summary

| Pages Parameter Summary |
| :--------------------- |
| **Description**<br>Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |
| **Type**<br>*int array* |
| **Value range**<br>Each array item represents a specified 0-based page index. |
