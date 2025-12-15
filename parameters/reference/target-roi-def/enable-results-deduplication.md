---
layout: default-layout
title: EnableResultsDeduplication - Dynamsoft Capture Vision Parameters
description: The parameter EnableResultsDeduplication of Dynamsoft Capture Vision defines whether to enable the result deduplication.
keywords: inheritance, deduplication, EnableResultsDeduplication
needGenerateH3Content: true
---
# EnableResultsDeduplication

Parameter `EnableResultsDeduplication` defines whether to enable the result deduplication.

## JSON Structure

**Location in template:**
```
TargetROIDefOptions[i]
    └── EnableResultsDeduplication
```

**Parent object:** [TargetROIDef]({{ site.dcvb_parameters }}file/target-roi-definition/index.html) object

**Example:**

```json
{
    "EnableResultsDeduplication": 1
}
```

> [!NOTE]
> - This snippet shows only the `EnableResultsDeduplication` parameter.
> - To use it, embed this parameter within a [TargetROIDef]({{ site.dcvb_parameters }}file/target-roi-definition/index.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| EnableResultsDeduplication Parameter Details |
| :----------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0,1] |
| **Default Value**<br>1 |
| **Remarks**<br> Supports deduplication between barcodes and text lines. |
