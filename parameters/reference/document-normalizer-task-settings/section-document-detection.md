---
layout: default-layout
title: DocumentDetectionSection - Dynamsoft Document Normalizer Parameters
description: The DocumentDetectionSection detects the edges of a document.
keywords: DocumentDetectionSection
---

# DocumentDetectionSection

`DocumentDetectionSection` detects the edges of a document. In JSON, it is represented as a Section object with `"Section": "ST_DOCUMENT_DETECTION"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object where Section = "ST_DOCUMENT_DETECTION")
```

**Parent object:** [SectionArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-array.html)

**Example:**

```json
{
    "Section": "ST_DOCUMENT_DETECTION",
    "ImageParameterName": "ip_ddnDefault",
    "StageArray": [
        {
            "Stage": "SST_DETECT_QUADS"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Section object configured for document detection.
> - To use it, add this object to the [SectionArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-array.html) of a [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Section

Specifies the section type. Fixed value: `ST_DOCUMENT_DETECTION`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"ST_DOCUMENT_DETECTION"` |

### ImageParameterName

Specifies the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object to apply in the stages of this section.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>Must be the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object defined under `ImageParameterOptions` |
| **Default Value**<br>`""` |

### StageArray

Specifies the stage objects within this section. The `DocumentDetectionSection` consists of the following stages:

| Stage | Description |
|-------|-------------|
| [AssembleLongLinesStage](./stage-assemble-long-lines.md) (`SST_ASSEMBLE_LONG_LINES`) | Assembles relatively long line segments to facilitate the assembly of more advanced line segments. |
| [AssembleLogicalLinesStage](./stage-assemble-logical-lines.md) (`SST_ASSEMBLE_LOGICAL_LINES`) | Assembles line segments based on certain criteria to serve the assembly of quadrilateral corners. |
| [DetectCornersStage](./stage-detect-corners.md) (`SST_DETECT_CORNERS`) | Detects corners of quadrilaterals that meet the specified conditions. |
| [DetectEdgesStage](./stage-detect-edges.md) (`SST_DETECT_EDGES`) | Detects edges of quadrilaterals that meet the specified conditions. |
| [DetectQuadsStage](./stage-detect-quads.md) (`SST_DETECT_QUADS`) | Detects complete quadrilaterals. |
