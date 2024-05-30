---
layout: default-layout
title: BarcodeFormat - Dynamsoft Barcode Reader Enumerations
description: The enumeration BarcodeFormat of Dynamsoft Barcode Reader defines the supported barcode formats.
keywords: Barcode formats
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BarcodeFormat
codeAutoHeight: true
---

# Enumeration BarcodeFormat

`BarcodeFormat` defines the supported barcode formats.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumBarcodeFormat {
    /** No barcode format specified.*/
    BF_NULL = 0x00,
    /** Represents all supported barcode formats. Useful for scanning operations where any type of barcode is acceptable. */
    BF_ALL = 0xFFFFFFFFFFFFFFFF,
    /** Default barcode formats that are commonly used. This is a subset of `BF_ALL` tailored for general use. */
    BF_DEFAULT = 0xFE3BFFFF,
    /** One-dimensional barcode formats, including BF_CODE_39, BF_CODE_128, BF_CODE_93, BF_CODABAR, BF_ITF, BF_EAN_13, BF_EAN_8, BF_UPC_A, BF_UPC_E, INDUSTRIAL_25, BF_CODE_39_Extended and BF_MSI_CODE. */
    BF_ONED = 0x3007FF,
    /** Code 39 format, widely used in various industries for inventory and manufacturing. */
    BF_CODE_39 = 0x1,
    /** Code 128 format, a high-density barcode for alphanumeric or numeric-only data. */
    BF_CODE_128 = 0x2,
    /** Code 93 format, similar to Code 39 but more compact and secure with support for the full ASCII character set. */
    BF_CODE_93 = 0x4,
    /** Codabar format, used for various numeric barcodes in libraries, blood banks, and parcels. */
    BF_CODABAR = 0x8,
    /** Interleaved 2 of 5 format, a numeric-only barcode used in warehousing, distribution, and logistics. */
    BF_ITF = 0x10,
    /** EAN-13 format, a superset of the UPC-A barcode used worldwide for marking retail goods. */
    BF_EAN_13 = 0x20,
    /** EAN-8 format, a compressed version of EAN-13 for smaller packages. */
    BF_EAN_8 = 0x40,
    /** UPC-A format, widely used in the United States and Canada for tracking trade items in stores. */
    BF_UPC_A = 0x80,
    /** UPC-E format, a smaller version of the UPC-A barcode used for smaller packages. */
    BF_UPC_E = 0x100,
    /** Industrial 2 of 5 format, an older, numeric-only barcode used in the industrial sector. */
    BF_INDUSTRIAL_25 = 0x200,
    /** Extended Code 39 format, capable of encoding the full ASCII character set by combining standard Code 39 characters. */
    BF_CODE_39_EXTENDED = 0x400,
    /** GS1 DataBar barcode formats, including BF_GS1_DATABAR_OMNIDIRECTIONAL, BF_GS1_DATABAR_TRUNCATED, BF_GS1_DATABAR_STACKED, BF_GS1_DATABAR_STACKED_OMNIDIRECTIONAL, BF_GS1_DATABAR_EXPANDED, BF_GS1_DATABAR_EXPANDED_STACKED, BF_GS1_DATABAR_LIMITED. These barcodes are designed for use in retail and healthcare for fresh foods and small items. */
    BF_GS1_DATABAR = 0x3F800,
    BF_GS1_DATABAR_OMNIDIRECTIONAL = 0x800,
    BF_GS1_DATABAR_TRUNCATED = 0x1000,
    BF_GS1_DATABAR_STACKED = 0x2000,
    BF_GS1_DATABAR_STACKED_OMNIDIRECTIONAL = 0x4000,
    BF_GS1_DATABAR_EXPANDED = 0x8000,
    BF_GS1_DATABAR_EXPANDED_STACKED = 0x10000,
    BF_GS1_DATABAR_LIMITED = 0x20000,
    /** Patch code, a special barcode used for document scanning applications to separate batches of documents. */
    BF_PATCHCODE = 0x40000,
    /** Micro PDF417, a compact version of PDF417 used for applications where space is limited. */
    BF_MICRO_PDF417 = 0x80000,
    /** MSI Code, a barcode used in inventory and warehouse to encode information in the distribution of goods. */
    BF_MSI_CODE = 0x100000,
    /** Code 11, used primarily for labeling telecommunications equipment. */
    BF_CODE_11 = 0x200000,
    /** Two-Digit Add-On, an extension to UPC and EAN codes for magazines and books. */
    BF_TWO_DIGIT_ADD_ON = 0x400000,
    /** Five-Digit Add-On, used with UPC and EAN codes for additional data, such as suggested retail price. */
    BF_FIVE_DIGIT_ADD_ON = 0x800000,
    /** Code 32, also known as Italian PharmaCode, used specifically in the Italian pharmaceutical industry. */
    BF_CODE_32 = 0x1000000,
    /** PDF417, a two-dimensional barcode used in a variety of applications, capable of encoding large amounts of data. */
    BF_PDF417 = 0x2000000,
    /** QR Code, a widely used two-dimensional barcode with high data capacity and error correction capability. */
    BF_QR_CODE = 0x4000000,
    /** DataMatrix, a two-dimensional barcode used for marking small items, providing high data density and reliability. */
    BF_DATAMATRIX = 0x8000000,
    /** Aztec, a two-dimensional barcode known for its compact size and suitability for encoding small amounts of data efficiently. */
    BF_AZTEC = 0x10000000,
    /** MaxiCode, a two-dimensional barcode used primarily for parcel and package tracking in logistics and postal services. */
    BF_MAXICODE = 0x20000000,
    /** Micro QR, a smaller version of the QR Code designed for applications where space is limited. */
    BF_MICRO_QR = 0x40000000,
    /** GS1 Composite, a group of barcodes used in conjunction with GS1 DataBar or linear barcodes to provide additional information. */
    BF_GS1_COMPOSITE = 0x80000000,
    /** Nonstandard barcode, a placeholder for barcodes that do not conform to established industry standards. */
    BF_NONSTANDARD_BARCODE = 0x100000000,
    /** DotCode, a two-dimensional barcode designed for high-speed printing applications. */
    BF_DOTCODE = 0x200000000,
    /** PharmaCode, a general category that includes both BF_PHARMACODE_ONE_TRACK and BF_PHARMACODE_TWO_TRACK. */
    BF_PHARMACODE = 0xC00000000,
    /** PharmaCode One Track, used in the pharmaceutical industry for packaging control. */
    BF_PHARMACODE_ONE_TRACK = 0x400000000,
    /** PharmaCode Two Track, an extension of PharmaCode for encoding additional data. */
    BF_PHARMACODE_TWO_TRACK = 0x800000000,
    /** Matrix 2 of 5, an older form of barcode used in warehouse sorting and conveyor systems. */
    BF_MATRIX_25 = 0x1000000000,
    /** Postal code barcodes, including various formats (BF_USPSINTELLIGENTMAIL, BF_POSTNET, BF_PLANET, BF_AUSTRALIANPOST, BF_RM4SCC and BF_KIX) used by postal services worldwide for efficient mail sorting and delivery. */
    BF_POSTALCODE = 0x3F0000000000000,
    /** USPS Intelligent Mail, a barcode used by the United States Postal Service to provide greater information and tracking capabilities. */
    BF_USPSINTELLIGENTMAIL = 0x10000000000000,
    /** Postnet, used by the USPS for automating the sorting of mail. */
    BF_POSTNET = 0x20000000000000,
    /** Planet, another USPS barcode, similar to Postnet, but with additional data capacity. */
    BF_PLANET = 0x40000000000000,
    /** Australian Post, barcodes used by the Australian postal service for mail sorting. */
    BF_AUSTRALIANPOST = 0x80000000000000,
    /** RM4SCC (Royal Mail 4 State Customer Code), used by the UK's Royal Mail for automated mail sorting. */
    BF_RM4SCC = 0x100000000000000,
    /** KIX (Klant index - Customer index), used by the Dutch postal service for sorting mail. */
    BF_KIX = 0x200000000000000
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumBarcodeFormat {
   /**All supported formats in BarcodeFormat.*/
   public static final long BF_ALL = 0xFFFFFFFFFFFFFFFF;
   /**The default settings.*/
   public static final long BF_DEFAULT = 0xFE3BFFFFL;
   /**Combined value of BF_CODABAR, BF_CODE_128, BF_CODE_39, BF_CODE_39_Extended, BF_CODE_93, BF_EAN_13, BF_EAN_8, INDUSTRIAL_25, BF_ITF, BF_UPC_A, BF_UPC_E, BF_MSI_CODE.*/
   public static final long BF_ONED = 0x3007FFL;
   /**Combined value of BF_GS1_DATABAR_OMNIDIRECTIONAL, BF_GS1_DATABAR_TRUNCATED, BF_GS1_DATABAR_STACKED, BF_GS1_DATABAR_STACKED_OMNIDIRECTIONAL, BF_GS1_DATABAR_EXPANDED, BF_GS1_DATABAR_EXPANDED_STACKED, BF_GS1_DATABAR_LIMITED*/
   public static final long BF_GS1_DATABAR = 0x3F800L;
   /**Disable all barcode format.*/
   public static final long BF_NULL = 0L;
   /**Code 39.*/
   public static final long BF_CODE_39 = 1L << 0;
   /**Code 128.*/
   public static final long BF_CODE_128 = 1L << 1;
   /**Code 93.*/
   public static final long BF_CODE_93 = 1L << 2;
   /**Codabar.*/
   public static final long BF_CODABAR = 1L << 3;
   /**Interleaved 2 of 5.*/
   public static final long BF_ITF = 1L << 4;
   /**EAN 13.*/
   public static final long BF_EAN_13 = 1L << 5;
   /**EAN_8 barcode.*/
   public static final long BF_EAN_8 = 1L << 6;
   /**UPC_A barcode.*/
   public static final long BF_UPC_A = 1L << 7;
   /**UPC_E barcode.*/
   public static final long BF_UPC_E = 1L << 8;
   /**Industrial 25 barcode*/
   public static final long BF_INDUSTRIAL_25 = 1L << 9;
   /**Code 39 Extened.*/
   public static final long BF_CODE_39_EXTENDED = 1L << 10;
   /**GS1 Databar - Omnidirectional.*/
   public static final long BF_GS1_DATABAR_OMNIDIRECTIONAL = 1L << 11;
   /**GS1 Databar - Truncated.*/
   public static final long BF_GS1_DATABAR_TRUNCATED = 1L << 12;
   /**GS1 Databar - Stacked.*/
   public static final long BF_GS1_DATABAR_STACKED = 1L << 13;
   /**GS1 Databar - Stacked omnidirectional.*/
   public static final long BF_GS1_DATABAR_STACKED_OMNIDIRECTIONAL = 1L << 14;
   /**GS1 Databar - Expanded.*/
   public static final long BF_GS1_DATABAR_EXPANDED = 1L << 15;
   /**GS1 Databar - Expanded stacked.*/
   public static final long BF_GS1_DATABAR_EXPANDED_STACKED = 1L << 16;
   /**GS1 Databar - Limited.*/
   public static final long BF_GS1_DATABAR_LIMITED = 1L << 17;
   /**Patch code.*/
   public static final long BF_PATCHCODE = 1L << 18;
   /**Micro PDF417 barcode.*/
   public static final long BF_MICRO_PDF417 = 1L << 19;
   /**MSI code.*/
   public static final long BF_MSI_CODE = 1L << 20;
   /**Code 11.*/
   public static final long BF_CODE_11 = 1L << 21;
   /**Decode barcode with 2 digital addons.*/
   public static final long BF_TWO_DIGIT_ADD_ON = 1L << 22,
   /**Decode barcode with 5 digital addons.*/
   public static final long BF_FIVE_DIGIT_ADD_ON = 1L << 23,
   /**Code 32*/
   public static final long BF_CODE_32 =  1L << 24;
   /**PDF417 barcode.*/
   public static final long BF_PDF417 = 1L << 25;
   /**QR code.*/
   public static final long BF_QR_CODE = 1L << 26;
   /**Data matrix.*/
   public static final long BF_DATAMATRIX = 1L << 27;
   /**AZTEC barcode.*/
   public static final long BF_AZTEC = 1L << 28;
   /**Maxicode.*/
   public static final long BF_MAXICODE = 1L << 29;
   /**Micro QR Code.*/
   public static final long BF_MICRO_QR = 1L << 30;
   /**GS1 Composite Code.*/
   public static final long BF_GS1_COMPOSITE = 1L << 31;
   /**Nonstandard barcode.*/
   public static final long BF_NONSTANDARD_BARCODE = 1L << 32;
   /**Dotcode.*/
   public static final long BF_DOTCODE = 1L << 33;
   /**Pharma code.*/
   public static final long BF_PHARMACODE = 0xC00000000L;
   /**Pharma code with one track.*/
   public static final long BF_PHARMACODE_ONE_TRACK = 1L << 34;
   /**Pharma code with two track.*/
   public static final long BF_PHARMACODE_TWO_TRACK = 1L << 35;
   /**Matrix25.*/
   public static final long BF_MATRIX_25 = 1L << 36;
   /**Postal code*/
   public static final long BF_POSTALCODE = 0x1F0000000000000L;
   /**USPS Intelligent Mail barcode.*/
   public static final long BF_USPSINTELLIGENTMAIL = 1L << 52;
   /**Postnet barcode.*/
   public static final long BF_POSTNET = 1L << 53;
   /**Planet barcode.*/
   public static final long BF_PLANET = 1L << 54;
   /**Australian post barcode.*/
   public static final long BF_AUSTRALIANPOST = 1L << 55;
   /**Royal Mail 4-State Customer barcode.*/
   public static final long BF_RM4SCC = 1L << 56;
   /**Kix.*/
   public static final long BF_KIX = 1L << 57;
}
```
>
```objc
typedef NS_OPTIONS(NSUInteger , DSBarcodeFormat)
{
   /**No barcode format in BarcodeFormat*/
   DSBarcodeFormatNull = 0,
   /**All supported formats in BarcodeFormat .*/
   DSBarcodeFormatAll = 0xFFFFFFFFFFFFFFFF,
   DSBarcodeFormatDefault = 0xFE3BFFFF,
   /**Code 39*/
   DSBarcodeFormatCode39 = 1,
   /**Code 128*/
   DSBarcodeFormatCode128 = 1 << 1,
   /**Code 93*/
   DSBarcodeFormatCode93 = 1 << 2,
   /**Codabar*/
   DSBarcodeFormatCodabar = 1 << 3,
   /**Interleaved 2 of 5*/
   DSBarcodeFormatITF = 1 << 4,
   /**EAN-13*/
   DSBarcodeFormatEAN13 = 1 << 5,
   /**EAN-8*/
   DSBarcodeFormatEAN8 = 1 << 6,
   /**UPC-A*/
   DSBarcodeFormatUPCA = 1 << 7,
   /**UPC-E*/
   DSBarcodeFormatUPCE = 1 << 8,
   /**Industrial 2 of 5*/
   DSBarcodeFormatIndustrial25 = 1 << 9,
   /**CODE39 Extended*/
   DSBarcodeFormatCode39Extended = 1 << 10,
    /**DataBar Omnidirectional*/
   DSBarcodeFormatGS1DatabarOmniDirectional = 1 << 11,
    /**DataBar Truncated*/
   DSBarcodeFormatGS1DatabarTruncated = 1 << 12,
    /**DataBar Stacked*/
   DSBarcodeFormatGS1DatabarStacked = 1 << 13,
    /**DataBar Stacked Omnidirectional*/
   DSBarcodeFormatGS1DatabarStackedOmniDirectional = 1 << 14,
    /**DataBar Expanded*/
   DSBarcodeFormatGS1DatabarExpanded = 1 << 15,
    /**DataBar Expaned Stacked*/
   DSBarcodeFormatGS1DatabarExpandedStacked = 1 << 16,
    /**DataBar Limited*/
   DSBarcodeFormatGS1DatabarLimited = 1 << 17,
   /**Patch code.*/
   DSBarcodeFormatPatchCode = 1 << 18,
    /**Micro PDF417*/
   DSBarcodeFormatMicroPDF417 = 1 << 19,
   /**MSI Code*/
   DSBarcodeFormatMSICode = 1 << 20,
   /**CODE_11 .*/
   DSBarcodeFormatCode11 = 1 << 21,
   /**Decode barcode with 2 digital addons.*/
   DSBarcodeFormatTwoDigitAddOn = 1 << 22,
   /**Decode barcode with 5 digital addons.*/
   DSBarcodeFormatFiveDigitAddOn = 1 << 23,
   /**Code 32*/
   DSBarcodeFormatCode32 =  1L << 24,
   /**PDF417*/
   DSBarcodeFormatPDF417 = 1 << 25,
   /**QRCode*/
   DSBarcodeFormatQRCode = 1 << 26,
   /**DataMatrix*/
   DSBarcodeFormatDataMatrix = 1 << 27,
   /**AZTEC*/
   DSBarcodeFormatAztec = 1 << 28,
   /**MAXICODE*/
   DSBarcodeFormatMaxiCode = 1 << 29,
   /**Micro QR Code*/
   DSBarcodeFormatMicroQR = 1 << 30,
   /**GS1 Composite Code*/
   DSBarcodeFormatGS1Composite = 1 << 31,
   /**Combined value of BF_CODABAR, BF_CODE_128, BF_CODE_39, BF_CODE_39_Extended, BF_CODE_93, BF_EAN_13, BF_EAN_8, INDUSTRIAL_25, BF_ITF, BF_UPC_A, BF_UPC_E, BF_MSI_CODE*/
   DSBarcodeFormatOneD = 0x3007FF,
   /**Combined value of BF_GS1_DATABAR_OMNIDIRECTIONAL, BF_GS1_DATABAR_TRUNCATED, BF_GS1_DATABAR_STACKED, BF_GS1_DATABAR_STACKED_OMNIDIRECTIONAL, BF_GS1_DATABAR_EXPANDED, BF_GS1_DATABAR_EXPANDED_STACKED, BF_GS1_DATABAR_LIMITED*/
   DSBarcodeFormatGS1Databar = 0x3F800,
   DSBarcodeFormatNonStandardBarcode = 1 << 32,
   /**DotCode Barcode.
   When you set this barcode format, the library will automatically add DSLocalizationModeStatisticsMarks to LocalizationMode if you don't set it,*/
   DSBarcodeFormatDotCode = 1 << 33,
   /**PHARMACODE_ONE_TRACK*/
   DSBarcodeFormatPharmaCodeOneTrack = 1 << 34,
   /**PHARMACODE_ONE_TRACK*/
   DSBarcodeFormatPharmaCodeTwoTrack = 1 << 35,
   /**Matrix25.*/
   DSBarcodeFormatMatrix25 = 1L << 36,
   /**PHARMACODE*/
   DSBarcodeFormatPharmaCode = 0xC00000000,
   /**Combined value of DSBarcodeFormatUSPSINTELLIGENTMAIL, DSBarcodeFormatPOSTNET, DSBarcodeFormatPLANET, DSBarcodeFormatAUSTRALIANPOST, DSBarcodeFormatRM4SCC.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   DSBarcodeFormatPostalCode = 0x1F0000000000000,
   /**USPS Intelligent Mail.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   DSBarcodeFormatUSPSIntelligentMail = 1 << 52,
   /**Postnet.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   DSBarcodeFormatPostnet = 1 << 53,
   /**Planet.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   DSBarcodeFormatPlant = 1 << 54,
   /**Australian Post.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   DSBarcodeFormatAustralianPost = 1 << 55,
   /**Royal Mail 4-State Customer Barcode.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   DSBarcodeFormatRM4SCC = 1 << 56,
   /**Kix*/
   DSBarcodeFormatKix = 1L << 57
};
```
>
```swift
public enum BarcodeFormat : Int
{
   /**No barcode format in BarcodeFormat*/
   Null = 0
   /**All supported formats in BarcodeFormat .*/
   all = 0xFFFFFFFFFFFFFFFF
   default = 0xFE3BFFFF
   /**Code 39*/
   code39 = 1
   /**Code 128*/
   code128 = 1 << 1
   /**Code 93*/
   code93 = 1 << 2
   /**Codabar*/
   codabar = 1 << 3
   /**Interleaved 2 of 5*/
   ITF = 1 << 4
   /**EAN-13*/
   EAN13 = 1 << 5
   /**EAN-8*/
   EAN8 = 1 << 6
   /**UPC-A*/
   UPCA = 1 << 7
   /**UPC-E*/
   UPCE = 1 << 8
   /**Industrial 2 of 5*/
   industrial25 = 1 << 9
   /**CODE39 Extended*/
   code39Extended = 1 << 10
   /**DataBar Omnidirectional*/
   gs1DatabarOmnidirectional = 1 << 11
   /**DataBar Truncated*/
   gs1DatabarTruncated = 1 << 12
   /**DataBar Stacked*/
   gs1DatabarStacked = 1 << 13
   /**DataBar Stacked Omnidirectional*/
   gs1DatabarStackedOmnidirectional = 1 << 14
   /**DataBar Expanded*/
   gs1DatabarExpanded = 1 << 15
   /**DataBar Expaned Stacked*/
   gs1DatabarExpandedStacked = 1 << 16
   /**DataBar Limited*/
   gs1DatabarLimited = 1 << 17
   /**Patch code.*/
   patchCode = 1 << 18
   /**Micro PDF417*/
   microPDF417 = 1 << 19
   /**MSI Code*/
   msiCode = 1 << 20
   /**CODE_11.*/
   code11 = 1 << 21
   /**Decode barcode with 2 digital addons.*/
   twoDigitAddOn = 1 << 22
   /**Decode barcode with 5 digital addons.*/
   fiveDigitAddOn = 1 << 23
   /**Code 32*/
   code32 =  1L << 24
   /**PDF417*/
   PDF417 = 1 << 25
   /**QRCode*/
   qrCode = 1 << 26
   /**DataMatrix*/
   dataMatrix = 1 << 27
   /**AZTEC*/
   aztec = 1 << 28
   /**MAXICODE*/
   maxiCode = 1 << 29
   /**Micro QR Code*/
   microQR = 1 << 30
   /**GS1 Composite Code*/
   gs1Composite = 1 << 31
   /**Combined value of BF_CODABAR, BF_CODE_128, BF_CODE_39, BF_CODE_39_Extended, BF_CODE_93, BF_EAN_13, BF_EAN_8, INDUSTRIAL_25, BF_ITF, BF_UPC_A, BF_UPC_E, BF_MSI_CODE*/
   oneD = 0x3007FF
   /**Combined value of BF_GS1_DATABAR_OMNIDIRECTIONAL, BF_GS1_DATABAR_TRUNCATED, BF_GS1_DATABAR_STACKED, BF_GS1_DATABAR_STACKED_OMNIDIRECTIONAL, BF_GS1_DATABAR_EXPANDED, BF_GS1_DATABAR_EXPANDED_STACKED, BF_GS1_DATABAR_LIMITED*/
   gs1Databar = 0x3F800,
   nonStandardBarcode = 1 << 32
   /**DotCode Barcode.
   When you set this barcode format, the library will automatically add DSLocalizationModeStatisticsMarks to LocalizationMode if you don't set it,*/
   dotCode = 1 << 33
   /**PHARMACODE_ONE_TRACK*/
   pharmaCodeOneTrack = 1 << 34
   /**PHARMACODE_ONE_TRACK*/
   pharmaCodeTwoTrack = 1 << 35
   /**Matrix25.*/
   matrix25 = 1L << 36
   /**PHARMACODE*/
   pharmaCode = 0xC00000000
   /**Combined value of DSBarcodeFormatUSPSINTELLIGENTMAIL, DSBarcodeFormatPOSTNET, DSBarcodeFormatPLANET, DSBarcodeFormatAUSTRALIANPOST, DSBarcodeFormatRM4SCC.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   postalCode = 0x1F0000000000000,
   /**USPS Intelligent Mail.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   uspsIntelligentMail = 1 << 52
   /**Postnet.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   postnet = 1 << 53
   /**Planet.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   planet = 1 << 54
   /**Australian Post.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   australianPost = 1 << 55
   /**Royal Mail 4-State Customer Barcode.
   When you set this barcode format, the library will automatically add LocalizationModeStatisticsPostalCode to LocalizationMode if you don't set it,*/
   RM4SCC = 1 << 56,
   /**Kix*/
   kix = 1L << 57
}
```
>
```cpp
enum BarcodeFormat : unsigned long long
{
   /**No barcode format in BarcodeFormat.*/
   BF_NULL = 0x00,
   /**All supported formats in BarcodeFormat.*/
   BF_ALL = 0xFFFFFFFFFFFFFFFF,
   /**Use the default barcode format settings.*/
   BF_DEFAULT = 0xFE3BFFFF,
   /**Combined value of BF_CODABAR, BF_CODE_128, BF_CODE_39, BF_CODE_39_Extended, BF_CODE_93, BF_EAN_13, BF_EAN_8, INDUSTRIAL_25, BF_ITF, BF_UPC_A, BF_UPC_E, BF_MSI_CODE;*/
   BF_ONED = 0x003007FF,
   /**Combined value of BF_GS1_DATABAR_OMNIDIRECTIONAL, BF_GS1_DATABAR_TRUNCATED, BF_GS1_DATABAR_STACKED, BF_GS1_DATABAR_STACKED_OMNIDIRECTIONAL, BF_GS1_DATABAR_EXPANDED, BF_GS1_DATABAR_EXPANDED_STACKED, BF_GS1_DATABAR_LIMITED*/
   BF_GS1_DATABAR = 0x0003F800,
   /**Code 39*/
   BF_CODE_39 = 0x1,
   /**Code 128*/
   BF_CODE_128 = 0x2,
   /**Code 93*/
   BF_CODE_93 = 0x4,
   /**Codabar*/
   BF_CODABAR = 0x8,
   /**Interleaved 2 of 5*/
   BF_ITF = 0x10,
   /**EAN-13*/
   BF_EAN_13 = 0x20,
   /**EAN-8*/
   BF_EAN_8 = 0x40,
   /**UPC-A*/
   BF_UPC_A = 0x80,
   /**UPC-E*/
   BF_UPC_E = 0x100,
   /**Industrial 2 of 5*/
   BF_INDUSTRIAL_25 = 0x200,
   /**CODE39 Extended*/
   BF_CODE_39_EXTENDED = 0x400,
   /**GS1 Databar Omnidirectional*/
   BF_GS1_DATABAR_OMNIDIRECTIONAL = 0x800,
   /**GS1 Databar Truncated*/
   BF_GS1_DATABAR_TRUNCATED = 0x1000,
   /**GS1 Databar Stacked*/
   BF_GS1_DATABAR_STACKED = 0x2000,
   /**GS1 Databar Stacked Omnidirectional*/
   BF_GS1_DATABAR_STACKED_OMNIDIRECTIONAL = 0x4000,
   /**GS1 Databar Expanded*/
   BF_GS1_DATABAR_EXPANDED = 0x8000,
   /**GS1 Databar Expaned Stacked*/
   BF_GS1_DATABAR_EXPANDED_STACKED = 0x10000,
   /**GS1 Databar Limited*/
   BF_GS1_DATABAR_LIMITED = 0x20000,
   /**Patch code.*/
   BF_PATCHCODE = 0x00040000,
   /**Code 32*/
   BF_CODE_32 = 0x1000000,
   /**PDF417*/
   BF_PDF417 = 0x02000000,
   /**QRCode*/
   BF_QR_CODE = 0x04000000,
   /**DataMatrix*/
   BF_DATAMATRIX = 0x08000000,
   /**AZTEC*/
   BF_AZTEC = 0x10000000,
   /**MAXICODE*/
   BF_MAXICODE = 0x20000000,
   /**Micro QR Code*/
   BF_MICRO_QR = 0x40000000,
   /**Micro PDF417*/
   BF_MICRO_PDF417 = 0x00080000,
   /**GS1 Composite Code*/
   BF_GS1_COMPOSITE = 0x80000000,
   /**MSI Code*/
   BF_MSI_CODE = 0x100000,
   /**Code 11*/
   BF_CODE_11 = 0x200000,
   /**Decode barcode with 2 digital addons.*/
   BF_TWO_DIGIT_ADD_ON = 0x400000,
   /**Decode barcode with 5 digital addons.*/
   BF_FIVE_DIGIT_ADD_ON = 0x800000,
   /**Matrix 25*/
   BF_MATRIX_25 = 0x1000000000,
   /**Combined value of BF2_USPSINTELLIGENTMAIL, BF2_POSTNET, BF2_PLANET, BF2_AUSTRALIANPOST, BF2_RM4SCC.*/
   BF_POSTALCODE = 0x3F0000000000000,
   /**Nonstandard barcode*/
   BF_NONSTANDARD_BARCODE = 0x100000000,
   /**USPS Intelligent Mail.*/
   BF_USPSINTELLIGENTMAIL = 0x10000000000000,
   /**Postnet.*/
   BF_POSTNET = 0x20000000000000,
   /**Planet.*/
   BF_PLANET = 0x40000000000000,
   /**Australian Post.*/
   BF_AUSTRALIANPOST = 0x80000000000000,
   /**Royal Mail 4-State Customer Barcode.*/
   BF_RM4SCC = 0x100000000000000,
   /**KIX.*/
   BF_KIX = 0x200000000000000,
   /**DotCode.*/
   BF_DOTCODE = 0x200000000,
   /**_PHARMACODE_ONE_TRACK.*/
   BF_PHARMACODE_ONE_TRACK = 0x400000000,
   /**PHARMACODE_TWO_TRACK.*/
   BF_PHARMACODE_TWO_TRACK = 0x800000000,
   /**PHARMACODE.*/
   BF_PHARMACODE = 0xC00000000
};
```
