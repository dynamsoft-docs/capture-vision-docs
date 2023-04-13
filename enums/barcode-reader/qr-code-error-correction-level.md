---
layout: default-layout
Title: QRCodeErrorCorrectionLevel - Dynamsoft Barcode Reader Enumerations
Description: The enumeration QRCodeErrorCorrectionLevel of Dynamsoft Barcode Reader describes the error correction level when processing the QR code.
Keywords: QR code error correction level
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: QRCodeErrorCorrectionLevel
---

# Enumeration QRCodeErrorCorrectionLevel

`QRCodeErrorCorrectionLevel` describes the error correction level when processing the QR code.

```cpp
typedef enum QRCodeErrorCorrectionLevel
{
    /**Error Correction Level H (high) */
    QRECL_ERROR_CORRECTION_H,
    /**Error Correction Level L (low) */
    QRECL_ERROR_CORRECTION_L,
    /**Error Correction Level M (medium-low) */
    QRECL_ERROR_CORRECTION_M,
    /**Error Correction Level Q (medium-high) */
    QRECL_ERROR_CORRECTION_Q
}QRCodeErrorCorrectionLevel;
```
