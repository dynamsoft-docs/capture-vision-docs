---
layout: default-layout
title: AssembleLogicalLinesStage - Dynamsoft Document Normalizer Parameters
description: The AssembleLogicalLinesStage assembles long line segments based on certain criteria.
keywords: Assemble Logical Lines Stage
---

# AssembleLogicalLinesStage

`AssembleLogicalLinesStage` assembles long line segments based on certain criteria to serve the assembly of quadrilateral corners. In JSON, it is represented as a Stage object with `"Stage": "SST_ASSEMBLE_LOGICAL_LINES"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_ASSEMBLE_LOGICAL_LINES")
```

**Parent object:** [StageArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html#stagearray) within [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html)

**Example:**

```json
{
    "Stage": "SST_ASSEMBLE_LOGICAL_LINES"
}
```

> [!NOTE]
> - This snippet shows a Stage object configured for assembling logical lines.
> - To use it, add this object to the `StageArray` within a [DocumentDetectionSection]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-document-detection.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Stage

Specifies the stage type. Fixed value: `SST_ASSEMBLE_LOGICAL_LINES`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"SST_ASSEMBLE_LOGICAL_LINES"` |