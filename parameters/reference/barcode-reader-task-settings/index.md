---
layout: default-layout
title: BarcodeReaderTaskSetting Parameters - Dynamsoft Capture Vision
description: Reference index for BarcodeReaderTaskSetting object in Dynamsoft Capture Vision parameters, including barcode format, localization, deformation resisting, deblur, and DPM code reading settings.
keywords: BarcodeReaderTaskSetting, barcode reader, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# BarcodeReaderTaskSetting Parameters

The `BarcodeReaderTaskSetting` object configures settings for barcode reading tasks performed on images in Dynamsoft Capture Vision.

## Example JSON

```json
{
    "BarcodeReaderTaskSettingOptions": [
        {
            "Name": "BR_0",
            "MaxThreadsInOneTask": 4,
            "ExpectedBarcodesCount": 512,
            "BarcodeFormatIds": ["BF_ALL"],
            "BarcodeFormatSpecificationNameArray": null,
            "DPMCodeReadingModes": [
                {
                    "Mode": "DPMCRM_SKIP"
                }
            ],
            "SectionArray": [
                {
                    "Section": "ST_REGION_PREDETECTION",
                    "ImageParameterName": "ip_dbrDefault",
                    "StageArray": [
                        {
                            "Stage": "SST_PREDETECT_REGIONS",
                            "RegionPredetectionModes": []
                        }
                    ]
                },
                {
                    "Section": "ST_BARCODE_LOCALIZATION",
                    "ImageParameterName": "ip_dbrDefault",
                    "StageArray": [
                        {
                            "Stage": "SST_LOCALIZE_CANDIDATE_BARCODES",
                            "LocalizationModes": []
                        },
                        {
                            "Stage": "SST_LOCALIZE_BARCODES"
                        }
                    ]
                },
                {
                    "Section": "ST_BARCODE_DECODING",
                    "ImageParameterName": "ip_dbrDefault",
                    "StageArray": [
                        {
                            "Stage": "SST_COMPLEMENT_BARCODE",
                            "BarcodeComplementModes": []
                        },
                        {
                            "Stage": "SST_RESIST_DEFORMATION",
                            "DeformationResistingModes": []
                        },
                        {
                            "Stage": "SST_SCALE_BARCODE_IMAGE",
                            "BarcodeScaleModes": []
                        },
                        {
                            "Stage": "SST_DECODE_BARCODES",
                            "DeblurModes": [],
                            "ReturnBarcodeZoneClarity": 0
                        }
                    ]
                }
            ],
            "TextResultOrderModes": [
                {
                    "Mode": "TROM_CONFIDENCE"
                }
            ],
            "BaseBarcodeReaderTaskSettingName": ""
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `BarcodeReaderTaskSetting` object inside `BarcodeReaderTaskSettingOptions`.

```text
BarcodeReaderTaskSetting
├── Name
├── MaxThreadsInOneTask
├── ExpectedBarcodesCount
├── BarcodeFormatIds
├── BarcodeFormatSpecificationNameArray
├── DPMCodeReadingModes
├── TextResultOrderModes
├── BaseBarcodeReaderTaskSettingName
└── SectionArray[]
    ├── item (Section = ST_REGION_PREDETECTION)
    │   ├── Section
    │   ├── ImageParameterName
    │   └── StageArray[]
    │       └── item (Stage = SST_PREDETECT_REGIONS)
    │           ├── Stage
    │           └── RegionPredetectionModes
    ├── item (Section = ST_BARCODE_LOCALIZATION)
    │   ├── Section
    │   ├── ImageParameterName
    │   └── StageArray[]
    │       ├── item (Stage = SST_LOCALIZE_CANDIDATE_BARCODES)
    │       │   ├── Stage
    │       │   └── LocalizationModes
    │       └── item (Stage = SST_LOCALIZE_BARCODES)
    │           └── Stage
    └── item (Section = ST_BARCODE_DECODING)
        ├── Section
        ├── ImageParameterName
        └── StageArray[]
            ├── item (Stage = SST_RESIST_DEFORMATION)
            │   ├── Stage
            │   └── DeformationResistingModes
            ├── item (Stage = SST_COMPLEMENT_BARCODE)
            │   ├── Stage
            │   └── BarcodeComplementModes
            ├── item (Stage = SST_SCALE_BARCODE_IMAGE)
            │   ├── Stage
            │   └── BarcodeScaleModes
            └── item (Stage = SST_DECODE_BARCODES)
                ├── Stage
                ├── DeblurModes
                └── ReturnBarcodeZoneClarity
```

> [!IMPORTANT]
> `Stage` values are constrained by the parent `Section` value, and stage-scoped parameters are constrained by the `Stage` value.

## Top-Level Parameters

| Parameter Name | Description |
| -------------- | ----------- |
| [`Name`](name.md) | The unique identifier for this `BarcodeReaderTaskSetting` object. |
| [`BarcodeFormatIds`](barcode-format-ids.md) | Specifies which barcode formats to read. |
| [`BarcodeFormatSpecificationNameArray`](barcode-format-specification-name-array.md) | Names of referenced `BarcodeFormatSpecification` objects for format-specific settings. |
| [`ExpectedBarcodesCount`](expected-barcodes-count.md) | Expected number of barcodes to detect per image. |
| [`MaxThreadsInOneTask`](max-threads-in-one-task.md) | Maximum number of parallel threads for this task. |
| [`SectionArray`](section-array.md) | Defines processing sections (region predetection, localization, decoding) and their stages. |
| [`DPMCodeReadingModes`](dpm-code-reading-modes.md) | Modes and priority for reading Direct Part Mark (DPM) codes. |
| [`TextResultOrderModes`](text-result-order-modes.md) | Order in which barcode results are returned. |
| [`BaseBarcodeReaderTaskSettingName`](base-barcode-reader-task-setting-name.md) | Name of another `BarcodeReaderTaskSetting` object to inherit parameters from. |

## Nested Parameter Quick Links

### Actual Nested Parameters in the Tree

| Parameter Name | Description |
|:--------------|:------------|
| [`RegionPredetectionModes`](../image-parameter/region-predetection-modes.md) | Controls how to find a region of interest (ROI) within the image or frame. |
| [`LocalizationModes`](localization-modes.md) | Determines how to localize barcodes. |
| [`DeformationResistingModes`](deformation-resisting-modes.md) | Defines how to handle distorted and deformed barcodes. |
| [`BarcodeComplementModes`](barcode-complement-modes.md) | Defines how to complement the missing parts of a barcode. |
| [`BarcodeScaleModes`](barcode-scale-modes.md) | Defines the scaling mode applied during barcode recognition. |
| [`DeblurModes`](deblur-modes.md) | Defines the mode and priority for deblurring. |
| [`ReturnBarcodeZoneClarity`](return-barcode-zone-clarity.md) | Defines whether to return the clarity of the barcode zone. |

### Conceptual Section/Stage Objects

| Object | Description |
|:-------|:------------|
| [`SectionRegionPredetection`](section-region-predetection.md) | Section object for `Section = ST_REGION_PREDETECTION`. |
| [`StagePredetectRegions`](stage-predetect-regions.md) | Stage object under `Section = ST_REGION_PREDETECTION` with `Stage = SST_PREDETECT_REGIONS`. |
| [`SectionBarcodeLocalization`](section-barcode-localization.md) | Section object for `Section = ST_BARCODE_LOCALIZATION`. |
| [`StageLocalizeCandidateBarcodes`](stage-localize-candidate-barcodes.md) | Stage object under `Section = ST_BARCODE_LOCALIZATION` with `Stage = SST_LOCALIZE_CANDIDATE_BARCODES`. |
| [`StageLocalizeBarcodes`](stage-localize-barcodes.md) | Stage object under `Section = ST_BARCODE_LOCALIZATION` with `Stage = SST_LOCALIZE_BARCODES`. |
| [`SectionBarcodeDecoding`](section-barcode-decoding.md) | Section object for `Section = ST_BARCODE_DECODING`. |
| [`StageResistDeformation`](stage-resist-deformation.md) | Stage object under `Section = ST_BARCODE_DECODING` with `Stage = SST_RESIST_DEFORMATION`. |
| [`StageComplementBarcode`](stage-complement-barcode.md) | Stage object under `Section = ST_BARCODE_DECODING` with `Stage = SST_COMPLEMENT_BARCODE`. |
| [`StageScaleBarcodeImage`](stage-scale-barcode-image.md) | Stage object under `Section = ST_BARCODE_DECODING` with `Stage = SST_SCALE_BARCODE_IMAGE`. |
| [`StageDecodeBarcodes`](stage-decode-barcodes.md) | Stage object under `Section = ST_BARCODE_DECODING` with `Stage = SST_DECODE_BARCODES`. |
