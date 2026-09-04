---
layout: default-layout
title: DocumentNormalizerTaskSetting Parameters - Dynamsoft Capture Vision
description: Reference index for DocumentNormalizerTaskSetting object in Dynamsoft Capture Vision parameters, including document detection, deskewing, image enhancement, and normalization settings.
keywords: DocumentNormalizerTaskSetting, document normalizer, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# DocumentNormalizerTaskSetting Parameters

The `DocumentNormalizerTaskSetting` object configures the settings for document detection and normalization in Dynamsoft Capture Vision.

## Example JSON

```json
{
    "DocumentNormalizerTaskSettingOptions": [
        {
            "Name": "ddn_task_default",
            "MaxThreadsInOneTask": 4,
            "ExpectedDocumentsCount": 1,
            "BaseDocumentNormalizerTaskSettingName": "",
            "SectionArray": [
                {
                    "Section": "ST_REGION_PREDETECTION",
                    "ImageParameterName": "ip_default",
                    "StageArray": [
                        {
                            "Stage": "SST_PREDETECT_REGIONS",
                            "RegionPredetectionModes": []
                        }
                    ]
                },
                {
                    "Section": "ST_DOCUMENT_DETECTION",
                    "ContentType": "CT_DOCUMENT",
                    "ImageParameterName": "ip_default",
                    "StageArray": [
                        { "Stage": "SST_ASSEMBLE_LONG_LINES" },
                        { "Stage": "SST_ASSEMBLE_LOGICAL_LINES" },
                        {
                            "Stage": "SST_DETECT_CORNERS",
                            "CornerAngleRange": {
                                "MaxValue": 110,
                                "MinValue": 70
                            }
                        },
                        { "Stage": "SST_DETECT_EDGES" },
                        {
                            "Stage": "SST_DETECT_QUADS",
                            "QuadrilateralDetectionModes": [
                                {
                                    "Mode": "QDM_GENERAL"
                                }
                            ]
                        }
                    ]
                },
                {
                    "Section": "ST_DOCUMENT_DESKEWING",
                    "ImageParameterName": "ip_default",
                    "StageArray": [
                        {
                            "Stage": "SST_DESKEW_IMAGE",
                            "DeskewMode": {
                                "ContentDirection": 0,
                                "Mode": "DSM_PERSPECTIVE_CORRECTION"
                            },
                            "PageSize": [-1, -1]
                        }
                    ]
                },
                {
                    "Section": "ST_IMAGE_ENHANCEMENT",
                    "ImageParameterName": "ip_0",
                    "StageArray": [
                        {
                            "Stage": "SST_ENHANCE_IMAGE",
                            "ColourMode": "ICM_COLOUR",
                            "Brightness": 0,
                            "Contrast": 0
                        }
                    ]
                }
            ]
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `DocumentNormalizerTaskSetting` object inside `DocumentNormalizerTaskSettingOptions`.

```text
DocumentNormalizerTaskSetting
├── Name
├── MaxThreadsInOneTask
├── ExpectedDocumentsCount
├── BaseDocumentNormalizerTaskSettingName
└── SectionArray[]
    ├── item (Section = ST_REGION_PREDETECTION)
    │   ├── Section
    │   ├── ImageParameterName
    │   └── StageArray[]
    │       └── item (Stage = SST_PREDETECT_REGIONS)
    │           ├── Stage
    │           └── RegionPredetectionModes
    ├── item (Section = ST_DOCUMENT_DETECTION)
    │   ├── Section
    │   ├── ContentType
    │   ├── ImageParameterName
    │   └── StageArray[]
    │       ├── item (Stage = SST_ASSEMBLE_LONG_LINES)
    │       │   └── Stage
    │       ├── item (Stage = SST_ASSEMBLE_LOGICAL_LINES)
    │       │   └── Stage
    │       ├── item (Stage = SST_DETECT_CORNERS)
    │       │   ├── Stage
    │       │   └── CornerAngleRange
    │       ├── item (Stage = SST_DETECT_EDGES)
    │       │   └── Stage
    │       └── item (Stage = SST_DETECT_QUADS)
    │           ├── Stage
    │           └── QuadrilateralDetectionModes
    ├── item (Section = ST_DOCUMENT_DESKEWING)
    │   ├── Section
    │   ├── ImageParameterName
    │   └── StageArray[]
    │       └── item (Stage = SST_DESKEW_IMAGE)
    │           ├── Stage
    │           ├── DeskewMode
    │           └── PageSize
    └── item (Section = ST_IMAGE_ENHANCEMENT)
        ├── Section
        ├── ImageParameterName
        └── StageArray[]
            └── item (Stage = SST_ENHANCE_IMAGE)
                ├── Stage
                ├── ColourMode
                ├── Brightness
                └── Contrast
```

> [!IMPORTANT]
> `Stage` values are constrained by the parent `Section` value, and stage-scoped parameters are constrained by the `Stage` value.


## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the DocumentNormalizerTaskSetting object. |
| [`BaseDocumentNormalizerTaskSettingName`](base-document-normalizer-task-setting-name.md) | The name of another DocumentNormalizerTaskSetting to inherit from. |
| [`MaxThreadsInOneTask`](max-threads-in-one-task.md) | The maximum threads in one task. |
| [`ExpectedDocumentsCount`](expected-documents-count.md) | The expected number of documents to detect. |
| [`SectionArray`](section-array.md) | The sections of the document normalizer task. |

## Nested Parameter Quick Links

### Actual Nested Parameters in the Tree

| Parameter Name | Description |
|:---------------|:------------|
| [`RegionPredetectionModes`](../image-parameter/region-predetection-modes.md) | Controls how to find a region of interest (ROI) within the image or frame. |
| [`ContentType`](content-type.md) | The content type of the document. |
| [`CornerAngleRange`](corner-angle-range.md) | The acceptable corner angle range for document detection. |
| [`QuadrilateralDetectionModes`](quadrilateral-detection-modes.md) | The modes for detecting document quadrilaterals. |
| [`DeskewMode`](deskew-mode.md) | The mode for deskewing the document. |
| [`PageSize`](page-size.md) | The page size for normalization. |
| [`ColourMode`](colour-mode.md) | The colour mode for the normalized image. |
| [`Brightness`](brightness.md) | The brightness of the normalized image. |
| [`Contrast`](contrast.md) | The contrast of the normalized image. |

### Conceptual Section/Stage Objects

| Object | Description |
|:-------|:------------|
| [`SectionRegionsPredetection`](section-regions-predetection.md) | Section object for `Section = ST_REGION_PREDETECTION`. |
| [`StagePredetectRegions`](stage-predetect-regions.md) | Stage object under `Section = ST_REGION_PREDETECTION` with `Stage = SST_PREDETECT_REGIONS`. |
| [`SectionDocumentDetection`](section-document-detection.md) | Section object for `Section = ST_DOCUMENT_DETECTION`. |
| [`StageAssembleLongLines`](stage-assemble-long-lines.md) | Stage object under `Section = ST_DOCUMENT_DETECTION` with `Stage = SST_ASSEMBLE_LONG_LINES`. |
| [`StageAssembleLogicalLines`](stage-assemble-logical-lines.md) | Stage object under `Section = ST_DOCUMENT_DETECTION` with `Stage = SST_ASSEMBLE_LOGICAL_LINES`. |
| [`StageDetectCorners`](stage-detect-corners.md) | Stage object under `Section = ST_DOCUMENT_DETECTION` with `Stage = SST_DETECT_CORNERS`. |
| [`StageDetectEdges`](stage-detect-edges.md) | Stage object under `Section = ST_DOCUMENT_DETECTION` with `Stage = SST_DETECT_EDGES`. |
| [`StageDetectQuads`](stage-detect-quads.md) | Stage object under `Section = ST_DOCUMENT_DETECTION` with `Stage = SST_DETECT_QUADS`. |
| [`SectionDocumentDeskewing`](section-document-deskewing.md) | Section object for `Section = ST_DOCUMENT_DESKEWING`. |
| [`StageDeskewImage`](stage-deskew-image.md) | Stage object under `Section = ST_DOCUMENT_DESKEWING` with `Stage = SST_DESKEW_IMAGE`. |
| [`SectionImageEnhancement`](section-image-enhancement.md) | Section object for `Section = ST_IMAGE_ENHANCEMENT`. |
| [`StageEnhanceImage`](stage-enhance-image.md) | Stage object under `Section = ST_IMAGE_ENHANCEMENT` with `Stage = SST_ENHANCE_IMAGE`. |


