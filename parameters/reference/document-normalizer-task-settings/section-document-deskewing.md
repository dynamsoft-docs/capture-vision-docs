---
layout: default-layout
title: DocumentDeskewingSection - Dynamsoft Document Normalizer Parameters
description: The DocumentDeskewingSection corrects perspective distortion by deskewing the document.
keywords: DocumentDeskewingSection
---

# DocumentDeskewingSection

`DocumentDeskewingSection` corrects perspective distortion by deskewing the document. In JSON, it is represented as a Section object with `"Section": "ST_DOCUMENT_DESKEWING"`.

## JSON Structure

**Location in template:**
```
DocumentNormalizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object where Section = "ST_DOCUMENT_DESKEWING")
```

**Parent object:** [SectionArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-array.html)

**Example:**

```json
{
    "Section": "ST_DOCUMENT_DESKEWING",
    "ImageParameterName": "ip_ddnDefault",
    "StageArray": [
        {
            "Stage": "SST_DESKEW_IMAGE"
        }
    ]
}
```

> [!NOTE]
> - This snippet shows a Section object configured for document deskewing.
> - To use it, add this object to the [SectionArray]({{ site.dcvb_parameters_reference }}document-normalizer-task-settings/section-array.html) of a [DocumentNormalizerTaskSetting]({{ site.dcvb_parameters }}file/task-settings/document-normalizer-task-settings.html).
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameters

### Section

Specifies the section type. Fixed value: `ST_DOCUMENT_DESKEWING`.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Required**<br>Yes |
| **Default Value**<br>`"ST_DOCUMENT_DESKEWING"` |

### ImageParameterName

Specifies the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object to apply in the stages of this section.

| Parameter Details |
| :------------- |
| **Type**<br>*string* |
| **Range**<br>Must be the name of an [ImageParameter]({{ site.dcvb_parameters }}file/image-parameter.html) object defined under `ImageParameterOptions` |
| **Default Value**<br>`""` |

### StageArray

Specifies the stage objects within this section. The `DocumentDeskewingSection` consists of the following stages:

| Stage | Description |
|-------|-------------|
| [DeskewImageStage](./stage-deskew-image.md) (`SST_DESKEW_IMAGE`) | Deskews the quadrilateral to transform it into a rectangle. |
