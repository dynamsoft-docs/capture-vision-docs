---
layout: default-layout
title: AssembleLinesStage - Dynamsoft Capture Vision Parameters
description: The AssembleLinesStage assembles short lines when processing documents.
keywords: Assemble Lines Stage
---

# AssembleLinesStage

`AssembleLinesStage` assembles short lines when processing documents. In JSON, it is represented as a Stage object with `"Stage": "SST_ASSEMBLE_LINES"`.

## JSON Structure

**Location in template:**
```
ImageParameterOptions[i]
    └── ApplicableStages[j] (Stage object where Stage = "SST_ASSEMBLE_LINES")
```

**Parent object:** [ApplicableStages]({{ site.dcvb_parameters_reference }}image-parameter/applicable-stages.html) within [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html)

**Example:**

```json
{
    "Stage": "SST_ASSEMBLE_LINES",
    "LineAssemblyMode": {
        "Mode": "LAM_GENERAL"
    }
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for assembling lines.
> - To use it, add this object to the `ApplicableStages` array within an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_ASSEMBLE_LINES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_ASSEMBLE_LINES"` |

### LineAssemblyMode

Defines how to assemble lines. See [`LineAssemblyMode`](line-assembly-mode.md) for details.
