---
layout: default-layout
title: ExpectedBarcodesCount - Dynamsoft Barcode Reader Parameters
description: The parameter ExpectedBarcodesCount defines the number of barcodes expected to be detected.
keywords: Expected barcodes count
---

# ExpectedBarcodesCount

`ExpectedBarcodesCount` defines the number of barcodes expected to be detected.

## JSON Structure

**Location in template:**
```
BarcodeReaderTaskSettingOptions[i]
    └── ExpectedBarcodesCount
```

**Parent object:** [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html)

**Example:**

```json
{
    "ExpectedBarcodesCount": 0
}
```

> [!NOTE]
> - This snippet shows only the `ExpectedBarcodesCount` parameter.
> - To use it, embed this parameter within a [BarcodeReaderTaskSetting]({{ site.dcvb_parameters }}file/task-settings/barcode-reader-task-settings.html) object in the complete JSON structure.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| ExpectedBarcodesCount Parameter Details |
| :--------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br>0 |

**Remarks**

- 0: detects at least one barcode.
- N ( N > 0 ): detects N barcodes.
- Dynamsoft Barcode Reader works as a loop trying different parameters to detect barcodes as many as possible. If ExpectedBarcodesCount is 0, the loop stops after a loop round finishes and detects at least one barcode. If ExpectedBarcodesCount is N, the loop stops once N barcodes are detected.
- ExpectedBarcodesCount applies to each page when decoding a multi-page file.
