---
layout: default-layout
Title: PartitionModes - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for PartitionModes.
Keywords: PartitionModes , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/partition-modes.html
---

# PartitionModes  

`PartitionModes` is used to select the mode used to apply partition process when decoding QRCode and DataMatrix.
## Example


```json
{
    "PartitionModes": ["PM_WHOLE_BARCODE"]
}
```

## Parameter Summary
The structure of the `PartitionModes` is shown as follow:

| PartitionModes  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string array* |
| **Range**<br>	"PM_WHOLE_BARCODE"<br>"PM_ALIGNMENT_PARTITION"|
| **Default Value**<br> ["PM_WHOLE_BARCODE","PM_ALIGNMENT_PARTITION"]|

**Remarks**
- PM_WHOLE_BARCODE: Take the whole barcode for decoding.
- PM_ALIGNMENT_PARTITION: Partition the barcode to blocks based on alignment.
- It works only for QRCode and DataMatrix.

### Default Settings

If the `PartitionModes` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "PartitionModes": ["PM_WHOLE_BARCODE","PM_ALIGNMENT_PARTITION"]
}
```