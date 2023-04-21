---
layout: default-layout
Title: MSICodeCheckDigitCalculation - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for MSICodeCheckDigitCalculation.
Keywords: MSICodeCheckDigitCalculation , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/msi-code-check-digit-calculation.html
---

# MSICodeCheckDigitCalculation  

`MSICodeCheckDigitCalculation` defines the scheme used for calculating a check digit of an MSI barcode.
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
| **Range**<br>	"MSICCDC_NO_CHECK_DIGIT"<br>"MSICCDC_MOD_10"<br>"MSICCDC_MOD_11"<br>"MSICCDC_MOD_1110"<br>"MSICCDC_MOD_1010"|
| **Default Value**<br> "MSICCDC_MOD_10"|


### Default Settings

If the `MSICodeCheckDigitCalculation` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "MSICodeCheckDigitCalculation": "MSICCDC_MOD_10"
}
```