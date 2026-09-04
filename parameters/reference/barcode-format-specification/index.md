---
layout: default-layout
title: BarcodeFormatSpecification Parameters - Dynamsoft Capture Vision
description: Reference index for BarcodeFormatSpecification object in Dynamsoft Capture Vision parameters, which defines format-specific decoding rules and constraints.
keywords: BarcodeFormatSpecification, barcode format, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# BarcodeFormatSpecification Parameters

The `BarcodeFormatSpecification` object defines format-specific decoding rules and constraints used by barcode reading tasks.

## Example JSON

```json
{
    "BarcodeFormatSpecificationOptions": [
        {
            "Name": "BFS_0",
            "BarcodeFormatIds": ["BF_QR_CODE"],
            "ExpectedBarcodesCount": 512,
            "MirrorMode": "MM_NORMAL",
            "MinResultConfidence": 30
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `BarcodeFormatSpecification` object inside `BarcodeFormatSpecificationOptions`.

```text
BarcodeFormatSpecification
├── Name
├── BarcodeFormatIds
└── Format-specific parameters like ExpectedBarcodesCount
```

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the `BarcodeFormatSpecification` object. |
| [`BarcodeFormatIds`](barcode-format-ids.md) | Specifies which barcode format(s) this specification applies to. |
| [`ExpectedBarcodesCount`](expected-barcodes-count.md) | Expected number of barcodes to decode. |
| [`MirrorMode`](mirror-mode.md) | Controls barcode mirroring handling. |
| [`MinResultConfidence`](min-result-confidence.md) | Minimum confidence threshold for accepted results. |
| [`StandardFormat`](standard-format.md) | Indicates whether standard format constraints are applied. |
| [`PartitionModes`](partition-modes.md) | Defines partitioning strategies during decoding. |
| [`VerifyCheckDigit`](verify-check-digit.md) | Defines whether to verify check digits. |
| [`IncludeTrailingCheckDigit`](include-trailing-check-digit.md) | Defines whether to include trailing check digits in text results. |
| [`IncludeImpliedAI01`](include-implied-ai01.md) | Defines whether to include implied AI(01) for GS1 parsing. |
| [`Code128Subset`](code128-subset.md) | Specifies the subset strategy for Code 128 decoding. |
| [`MsiCodeCheckDigitCalculation`](msi-code-check-digit-calculation.md) | Specifies MSI check digit calculation rules. |
| [`RequireStartStopChars`](require-start-stop-chars.md) | Defines whether start/stop characters are required. |
| [`EnableAddOnCode`](enable-addon-code.md) | Defines whether add-on codes are decoded with primary barcodes. |
| [`EnableDataMatrixECC000140`](enable-data-matrix-ecc000-140.md) | Defines whether DataMatrix ECC000-140 variants are enabled. |
| [`DataMatrixModuleIsotropic`](data-matrix-module-isotropic.md) | Controls isotropic module assumption for DataMatrix. |
| [`DataMatrixSizeOptions`](data-matrix-size-options.md) | Specifies acceptable DataMatrix symbol size options. |
| [`EnableQRCodeModel1`](enable-qr-code-model-1.md) | Defines whether QR Code Model 1 decoding is enabled. |
| [`AustralianPostEncodingTable`](australian-post-encoding-table.md) | Specifies encoding table selection for Australian Post barcodes. |
| [`ReturnPartialBarcodeValue`](return-partial-barcode-value.md) | Defines whether partial barcode values can be returned. |
| [`FindUnevenModuleBarcode`](find-uneven-module-barcode.md) | Defines whether to detect barcodes with uneven modules. |
| [`AutoDetectColorInversion`](auto-detect-color-inversion.md) | Defines whether to auto-detect foreground/background inversion. |
| [`HasVerticalQuietZone`](has-vertical-quietzone.md) | Defines whether vertical quiet zone is required/assumed. |
| [`HeadModuleRatio`](head-module-ratio.md) | Defines ratio constraints for leading modules. |
| [`TailModuleRatio`](tail-module-ratio.md) | Defines ratio constraints for trailing modules. |
| [`MinQuietZoneWidth`](min-quiet-zone-width.md) | Minimum quiet-zone width requirement. |
| [`MinRatioOfBarcodeZoneWidthToHeight`](min-ratio-of-barcode-zone-width-to-height.md) | Minimum width-to-height ratio for barcode zones. |
| [`BarcodeZoneMinDistanceToImageBorders`](barcode-zone-min-distance-to-image-borders.md) | Minimum distance from barcode zone to image borders. |
| [`BarcodeZoneWidthToHeightRatioRangeArray`](barcode-zone-width-to-height-ratio-range-array.md) | Acceptable barcode-zone width/height ratio range(s). |
| [`BarcodeZoneBarCountRangeArray`](barcode-zone-bar-count-range-array.md) | Acceptable barcode bar-count range(s). |
| [`BarcodeWidthRangeArray`](barcode-width-range-array.md) | Acceptable barcode width range(s). |
| [`BarcodeHeightRangeArray`](barcode-height-range-array.md) | Acceptable barcode height range(s). |
| [`BarcodeAngleRangeArray`](barcode-angle-range-array.md) | Acceptable barcode angle range(s). |
| [`BarcodeTextLengthRangeArray`](barcode-text-length-range-array.md) | Acceptable decoded-text length range(s). |
| [`BarcodeBytesLengthRangeArray`](barcode-bytes-length-range-array.md) | Acceptable decoded-byte length range(s). |
| [`BarcodeTextRegexPattern`](barcode-text-regex-pattern.md) | Regex pattern to validate decoded barcode text. |
| [`ModuleSizeRangeArray`](module-size-range-array.md) | Acceptable module-size range(s). |
| [`PatchCodeSearchingMargins`](patch-code-searching-margins.md) | Search margins for Patch Code localization. |
| [`AllModuleDeviation`](all-module-deviation.md) | Allowed deviation threshold for module consistency checks. |
