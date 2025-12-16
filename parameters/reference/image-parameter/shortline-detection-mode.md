---
layout: default-layout
title: ShortlineDetectionMode - Dynamsoft Capture Vision Parameters
description: The parameter ShortlineDetectionMode of Dynamsoft Capture Vision is for controlling how to detect the shortlines.
keywords: ShortlineDetectionMode, short lines, parameter reference, parameter
---


# ShortlineDetectionMode

Parameter `ShortlineDetectionMode` is for controlling how to detect the shortlines.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_DETECT_SHORTLINES")
        └── ShortlineDetectionMode
```

**Parent object:** [DetectShortLinesStage](stage-detect-shortlines.md)

**Example:**

```json
{
    "ShortlineDetectionMode": {
        "Mode": "SDM_GENERAL",
        "Sensitivity": 3
    }
}
```

> [!NOTE]
> - This snippet shows only the `ShortlineDetectionMode` parameter.
> - To use it, embed this parameter within a [DetectShortLinesStage](stage-detect-shortlines.md) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The `ShortlineDetectionMode` object includes the following parameters:

### Mode

Specifies the shortline detection mode to use.

| Mode Parameter Details |
| :--------------------- |
| **Type**<br>*String* |
| **Value Range**<br>"SDM_GENERAL" |
| **Default Value**<br>"SDM_GENERAL" |

### Sensitivity

Specifies the sensitivity level used for shortline detection. A higher value means the algorithm will be more sensitive when detecting short lines.

| Sensitivity Parameter Details |
| :---------------------------- |
| **Type**<br>*int* |
| **Value Range**<br>[1, 9] |
| **Default Value**<br>3 for BarcodeReader Task<br>6 for DocumentNormalizer Task |
| **Valid For**<br>"SDM_GENERAL" |
