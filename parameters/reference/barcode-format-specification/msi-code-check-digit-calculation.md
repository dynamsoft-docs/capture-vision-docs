---
layout: default-layout
Title: MSICodeCheckDigitCalculation - Dynamsoft Barcode Reader Parameters
Description: The parameter ModuleSizeRangeArray of Dynamsoft Barcode Reader defines the scheme used for calculating a check digit of an MSI barcode.
Keywords: MSICodeCheckDigitCalculation , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/msi-code-check-digit-calculation.html
---

# MSICodeCheckDigitCalculation

Parameter `MSICodeCheckDigitCalculation` defines the scheme used for calculating a check digit of an MSI barcode.

## Example

```json
{
    "MSICodeCheckDigitCalculation": "MSICCDC_MOD_1110"
}
```

## Parameter Summary

The structure of the `MSICodeCheckDigitCalculation` is shown as follow:

| MSICodeCheckDigitCalculation  Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>MSICCDC_NO_CHECK_DIGIT<br>MSICCDC_MOD_10<br>MSICCDC_MOD_11<br>MSICCDC_MOD_1110<br>MSICCDC_MOD_1010 |
| **Default Value**<br>MSICCDC_MOD_10 |
