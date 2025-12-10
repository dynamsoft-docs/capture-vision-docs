---
layout: default-layout
title: AssembleLongLinesStage - Dynamsoft Document Normalizer Parameters
description: The AssembleLongLinesStage assembles relatively long line segments.
keywords: Assemble Long Lines Stage
---

# AssembleLongLinesStage

`AssembleLongLinesStage` assembles relatively long line segments to facilitate the assembly of more advanced line segments. In JSON, it is represented as a Stage object with `"Stage": "SST_ASSEMBLE_LONG_LINES"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_ASSEMBLE_LONG_LINES")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html#stagearray) within [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html)

**Example:**

```json
{
    "Stage": "SST_ASSEMBLE_LONG_LINES"
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for assembling long lines.
> - To use it, add this object to the `StageArray` within a [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_ASSEMBLE_LONG_LINES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_ASSEMBLE_LONG_LINES"` |