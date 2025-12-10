---
layout: default-layout
title: MSICodeCheckDigitCalculation - Dynamsoft Barcode Reader Parameters
description: The parameter ModuleSizeRangeArray of Dynamsoft Barcode Reader defines the scheme used for calculating a check digit of an MSI barcode.
keywords: MSICodeCheckDigitCalculation , parameter reference, parameter
---

# MSICodeCheckDigitCalculation

Parameter `MSICodeCheckDigitCalculation` defines the scheme used for calculating a check digit of an MSI barcode.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── MsiCodeCheckDigitCalculation
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "MSICodeCheckDigitCalculation": "MSICCDC_MOD_1110"
}
```

> [!NOTE]
> - This snippet shows only the `MsiCodeCheckDigitCalculation` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `MSICodeCheckDigitCalculation` is shown as follow:

| MSICodeCheckDigitCalculation  Parameter Details |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>MSICCDC_NO_CHECK_DIGIT<br>MSICCDC_MOD_10<br>MSICCDC_MOD_11<br>MSICCDC_MOD_1110<br>MSICCDC_MOD_1010 |
| **Default Value**<br>MSICCDC_MOD_10 |
