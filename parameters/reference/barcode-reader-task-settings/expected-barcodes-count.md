---
layout: default-layout
title: ExpectedBarcodesCount - Dynamsoft Barcode Reader Parameters
description: The parameter ExpectedBarcodesCount of Dynamsoft Barcode Reader defines the number of barcodes expected to be detected.
keywords: Expected barcodes count
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/expected-barcodes-count.html
---

# ExpectedBarcodesCount

Parameter `ExpectedBarcodesCount` defines the number of barcodes expected to be detected.

## Example

```json
{
    "ExpectedBarcodesCount": 0
}
```

## Parameter Summary

| ExpectedBarcodesCount Parameter Summary |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br>0 |

**Remarks**

- 0: detects at least one barcode.
- N ( N > 0 ): detects N barcodes.
- Dynamsoft Barcode Reader works as a loop trying different parameters to detect barcodes as many as possible. If ExpectedBarcodesCount is 0, the loop stops after a loop round finishes and detects at least one barcode. If ExpectedBarcodesCount is N, the loop stops once N barcodes are detected.
- ExpectedBarcodesCount applies to each page when decoding a multi-page file.
