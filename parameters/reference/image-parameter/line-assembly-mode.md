---
layout: default-layout
title: LineAssemblyMode - Dynamsoft Capture Vision Parameters
description: The parameter LineAssemblyMode of Dynamsoft Capture Vision is for controlling how to assemble the lines.
keywords: LineAssemblyMode, assemble lines, parameter reference, parameter
---


# LineAssemblyMode

Parameter `LineAssemblyMode` is for controlling how to assemble the lines.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_ASSEMBLE_LINES")
        └── LineAssemblyMode
```

**Parent object:** [AssembleLinesStage](stage-assemble-lines.md)

**Example:**

```json
{
    "LineAssemblyMode": {
        "Mode": "LAM_GENERAL",
        "Sensitivity": 3
    }
}
```

> [!NOTE]
> - This snippet shows only the `LineAssemblyMode` parameter.
> - To use it, embed this parameter within an [AssembleLinesStage](stage-assemble-lines.md) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The `LineAssemblyMode` object includes the following parameters:

### Mode

Specifies the line assembly mode to use.

| Mode Parameter Details |
| :--------------------- |
| **Type**<br>*String* |
| **Value Range**<br>"LAM_GENERAL" |
| **Default Value**<br>"LAM_GENERAL" |

### Sensitivity

Specifies the sensitivity level used for line assembling. A higher value means the algorithm will be more sensitive when detecting and assembling lines.

| Sensitivity Parameter Details |
| :---------------------------- |
| **Type**<br>*int* |
| **Value Range**<br>[1, 9] |
| **Default Value**<br>3 for BarcodeReader Task<br>6 for DocumentNormalizer Task |
| **Valid For**<br>"LAM_GENERAL" |
