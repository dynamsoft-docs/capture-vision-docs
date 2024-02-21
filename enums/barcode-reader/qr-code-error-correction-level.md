---
layout: default-layout
title: QRCodeErrorCorrectionLevel - Dynamsoft Barcode Reader Enumerations
description: The enumeration QRCodeErrorCorrectionLevel of Dynamsoft Barcode Reader describes the error correction level when processing the QR code.
keywords: QR code error correction level
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: QRCodeErrorCorrectionLevel
codeAutoHeight: true
---

# Enumeration QRCodeErrorCorrectionLevel

`QRCodeErrorCorrectionLevel` describes the error correction level when processing the QR code.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumQRCodeErrorCorrectionLevel{
    /** High error correction level, allowing for up to 30% data recovery. Suitable for environments where QR codes might be subject to significant damage. */
    QRECL_ERROR_CORRECTION_H = 0,
    /** Low error correction level, allowing for up to 7% data recovery. Optimal for scenarios where QR code integrity is less likely to be compromised. */
    QRECL_ERROR_CORRECTION_L = 1,
    /** Medium-low error correction level, allowing for up to 15% data recovery. Balances the need for data integrity with the desire to maximize data capacity. */
    QRECL_ERROR_CORRECTION_M = 2,
    /** Medium-high error correction level, allowing for up to 25% data recovery. Designed for situations where some QR code damage might be expected. */
    QRECL_ERROR_CORRECTION_Q = 3
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumQRCodeErrorCorrectionLevel
{
   /**Error Correction Level H (high) */
   public static final int QRECL_ERROR_CORRECTION_H = 0;
   /**Error Correction Level L (low) */
   public static final int QRECL_ERROR_CORRECTION_L = 1;
   /**Error Correction Level M (medium-low) */
   public static final int QRECL_ERROR_CORRECTION_M = 2;
   /**Error Correction Level Q (medium-high) */
   public static final int QRECL_ERROR_CORRECTION_Q = 3;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSQRCodeErrorCorrectionLevel)
{
   /**Error Correction Level H (high) */
    DSQRCodeErrorCorrectionLevelErrorCorrectionH = 0,
   /**Error Correction Level L (low) */
    DSQRCodeErrorCorrectionLevelErrorCorrectionL = 1,
   /**Error Correction Level M (medium-low) */
    DSQRCodeErrorCorrectionLevelErrorCorrectionM = 2,
   /**Error Correction Level Q (medium-high) */
    DSQRCodeErrorCorrectionLevelErrorCorrectionQ = 3
};
```
>
```swift
public enum QRCodeErrorCorrectionLevel : Int
{
   /**Error Correction Level H (high) */
   errorCorrectionH = 0
   /**Error Correction Level L (low) */
   errorCorrectionL = 1
   /**Error Correction Level M (medium-low) */
   errorCorrectionM = 2
   /**Error Correction Level Q (medium-high) */
   errorCorrectionQ = 3
}
```
>
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
