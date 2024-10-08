---
layout: default-layout
title: LocalizationMode - Dynamsoft Barcode Reader Enumerations
description: The enumeration LocalizationMode of Dynamsoft Barcode Reader describes the localization modes of the barcodes.
keywords: Localization mode
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: LocalizationMode
codeAutoHeight: true
---

# Enumeration LocalizationMode

`LocalizationMode` specifies the strategies used to identify the locations of barcodes within an image.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >- C#
   >- Python
   >
>
```javascript
enum EnumLocalizationMode {
    /** Omits the localization process entirely. */
    LM_SKIP = 0x00,
    /** Automatic localization mode selection; not yet implemented. */
    LM_AUTO = 0x01,
    /** Identifies barcodes by finding connected blocks, offering optimal results, especially recommended for highest priority in most scenarios. */
    LM_CONNECTED_BLOCKS = 0x02,
    /** Detects barcodes through analysis of patterns of contiguous black and white regions, tailored for QR Codes and DataMatrix codes. */
    LM_STATISTICS = 0x04,
    /** Locates barcodes by identifying linear patterns, designed primarily for 1D barcodes and PDF417 codes. */
    LM_LINES = 0x08,
    /** Provides rapid barcode localization, suited for interactive applications where speed is crucial. */
    LM_SCAN_DIRECTLY = 0x10,
    /** Targets barcode localization through detection of specific mark groups, optimized for Direct Part Marking (DPM) codes. */
    LM_STATISTICS_MARKS = 0x20,
    /** Combines methods of locating connected blocks and linear patterns to efficiently localize postal codes. */
    LM_STATISTICS_POSTAL_CODE = 0x40,
    /** Initiates barcode localization from the image center, facilitating faster detection in certain layouts. */
    LM_CENTRE = 0x80,
    /** Specialized for quick localization of 1D barcodes, enhancing performance in fast-scan scenarios. */
    LM_ONED_FAST_SCAN = 0x100,
    /** Reserved for future use in localization mode settings. */
    LM_REV = -2147483648
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumLocalizationMode {
   /**Not supported yet. */
   public static final int LM_AUTO = 1;
   /**Localizes barcodes by searching for connected blocks. This algorithm usually gives best result and it is recommended to set ConnectedBlocks to the highest priority. */
   public static final int LM_CONNECTED_BLOCKS = 2;
   /**Localizes barcodes by groups of contiguous black-white regions. This is optimized for QRCode and DataMatrix. */
   public static final int LM_STATISTICS = 4;
   /**Localizes barcodes by searching for groups of lines. This is optimized for 1D and PDF417 barcodes. */
   public static final int LM_LINES = 8;
   /**Localizes barcodes quickly. This mode is recommended in interactive scenario. Check @ref LM for available argument settings.*/
   public static final int LM_SCAN_DIRECTLY = 16;
   /**Localizes barcodes by groups of marks.This is optimized for DPM codes. */
   public static final int LM_STATISTICS_MARKS = 32;
   /**Localizes barcodes by groups of connected blocks and lines.This is optimized for postal codes. */
   public static final int LM_STATISTICS_POSTAL_CODE = 64;
   /**Localizes barcodes from the centre of the image. Check @ref LM for available argument settings. */
   public static final int LM_CENTRE = 128;
   /**Localizes 1D barcodes fast. Check @ref LM for available argument settings. */
   public static final int LM_ONED_FAST_SCAN = 256;
   /**Skips localization. */
   public static final int LM_SKIP = 0;
   /**Reserved setting for localization mode. */
   public static final int LM_REV = 2147483648;
}
```
>
```objc
typedef NS_ENUM(NSInteger , DSLocalizationMode)
{
   /**Not supported yet. */
   DSLocalizationModeAuto = 0x01,
   /**Localizes barcodes by searching for connected blocks. This algorithm usually gives best result and it is recommended to set ConnectedBlocks to the highest priority. */
   DSLocalizationModeConnectedBlocks = 0x02,
   /**Localizes barcodes by groups of contiguous black-white regions. This is optimized for QRCode and DataMatrix. */
   DSLocalizationModeStatistics = 0x04,
   /**Localizes barcodes by searching for groups of lines. This is optimized for 1D and PDF417 barcodes. */
   DSLocalizationModeLines = 0x08,
   /**Localizes barcodes quickly. This mode is recommended in interactive scenario. Check @ref LM for available argument settings.*/
   DSLocalizationModeScanDirectly = 0x10,
   /**Localizes barcodes by groups of marks.This is optimized for DPM codes. */
   DSLocalizationModeStatisticsMarks = 0x20,
   /**Localizes barcodes by groups of connected blocks and lines.This is optimized for postal codes. */
   DSLocalizationModeStatisticsPostalCode = 0x40,
   /**Localizes barcodes from the centre of the image. Check @ref LM for available argument settings. */
   DSLocalizationModeCentre = 0x80,
   /**Localizes 1D barcodes fast. Check @ref LM for available argument settings. */
   DSLocalizationModeOneDFastScan = 0x100,
   /**Reserved setting for localization mode.*/
   DSLocalizationModeRev = -2147483648,
   /**Skips localization. */
   DSLocalizationModeSkip = 0x00
};
```
>
```swift
public enum LocalizationMode : Int
{
   /**Not supported yet. */
   auto = 0x01
   /**Localizes barcodes by searching for connected blocks. This algorithm usually gives best result and it is recommended to set ConnectedBlocks to the highest priority. */
   connectedBlocks = 0x02
   /**Localizes barcodes by groups of contiguous black-white regions. This is optimized for QRCode and DataMatrix. */
   statistics = 0x04
   /**Localizes barcodes by searching for groups of lines. This is optimized for 1D and PDF417 barcodes. */
   lines = 0x08
   /**Localizes barcodes quickly. This mode is recommended in interactive scenario. Check @ref LM for available argument settings.*/
   scanDirectly = 0x10
   /**Localizes barcodes by groups of marks.This is optimized for DPM codes. */
   statisticsMarks = 0x20
   /**Localizes barcodes by groups of connected blocks and lines.This is optimized for postal codes. */
   postalCode = 0x40
   /**Localizes barcodes from the centre of the image. Check @ref LM for available argument settings. */
   centre = 0x80,
   /**Localizes 1D barcodes fast. Check @ref LM for available argument settings. */
   oneDFastScan = 0x100
   /**Reserved setting for localization mode.*/
   rev = -2147483648
   /**Skips localization. */
   skip = 0x00
}
```
>
```cpp
typedef enum LocalizationMode
{
   /**Not supported yet. */
   LM_AUTO = 0x01,
   /**Localizes barcodes by searching for connected blocks. This algorithm usually gives best result and it is recommended to set ConnectedBlocks to the highest priority. */
   LM_CONNECTED_BLOCKS = 0x02,
   /**Localizes barcodes by groups of contiguous black-white regions. This is optimized for QRCode and DataMatrix. */
   LM_STATISTICS = 0x04,
   /**Localizes barcodes by searching for groups of lines. This is optimized for 1D and PDF417 barcodes. */
   LM_LINES = 0x08,
   /**Localizes barcodes quickly. This mode is recommended in interactive scenario. Check @ref LM for available argument settings. */
   LM_SCAN_DIRECTLY = 0x10,
   /**Localizes barcodes by groups of marks.This is optimized for DPM codes. */
   LM_STATISTICS_MARKS = 0x20,
   /**Localizes barcodes by groups of connected blocks and lines.This is optimized for postal codes. */
   LM_STATISTICS_POSTAL_CODE = 0x40,
   /**Localizes barcodes from the centre of the image. Check @ref LM for available argument settings. */
   LM_CENTRE = 0x80,
   /**Localizes 1D barcodes fast. Check @ref LM for available argument settings. */
   LM_ONED_FAST_SCAN = 0x100,
   /**Reserved setting for localization mode. */
#if defined(_WIN32) || defined(_WIN64)
   LM_REV = 0x80000000,
#else
   LM_REV = -2147483648,
#endif
   /**Skips localization. */
   LM_SKIP = 0x00
}LocalizationMode;
```
>
```csharp
public enum EnumLocalizationMode
{
    /**Not supported yet. */
    LM_AUTO = 0x01,
    /**Localizes barcodes by searching for connected blocks. This algorithm usually gives best result and it is recommended to set ConnectedBlocks to the highest priority. */
    LM_CONNECTED_BLOCKS = 0x02,
    /**Localizes barcodes by groups of contiguous black-white regions. This is optimized for QRCode and DataMatrix. */
    LM_STATISTICS = 0x04,
    /**Localizes barcodes by searching for groups of lines. This is optimized for 1D and PDF417 barcodes. */
    LM_LINES = 0x08,
    /**Localizes barcodes quickly. This mode is recommended in interactive scenario.*/
    LM_SCAN_DIRECTLY = 0x10,
    /**Localizes barcodes by groups of marks.This is optimized for DPM codes. */
    LM_STATISTICS_MARKS = 0x20,
    /**Localizes barcodes by groups of connected blocks and lines.This is optimized for postal codes. */
    LM_STATISTICS_POSTAL_CODE = 0x40,
    /**Localizes barcodes from the centre of the image.*/
    LM_CENTRE = 0x80,
    /**Localizes 1D barcodes fast.*/
    LM_ONED_FAST_SCAN = 0x100,
    /**Reserved setting for localization mode.*/
    LM_REV = -2147483648,
    /**Skips localization. */
    LM_SKIP = 0x00
}
```
>
```python
class EnumLocalizationMode(IntEnum):
{
    #Not supported yet. 
    LM_AUTO = 0x01
    #Localizes barcodes by searching for connected blocks. This algorithm usually gives best result and it is recommended to set ConnectedBlocks to the highest priority. 
    LM_CONNECTED_BLOCKS = 0x02
    #Localizes barcodes by groups of contiguous black-white regions. This is optimized for QRCode and DataMatrix. 
    LM_STATISTICS = 0x04
    #Localizes barcodes by searching for groups of lines. This is optimized for 1D and PDF417 barcodes. 
    LM_LINES = 0x08
    #Localizes barcodes quickly. This mode is recommended in interactive scenario.
    LM_SCAN_DIRECTLY = 0x10
    #Localizes barcodes by groups of marks.This is optimized for DPM codes. 
    LM_STATISTICS_MARKS = 0x20
    #Localizes barcodes by groups of connected blocks and lines.This is optimized for postal codes. 
    LM_STATISTICS_POSTAL_CODE = 0x40
    #Localizes barcodes from the centre of the image.
    LM_CENTRE = 0x80
    #Localizes 1D barcodes fast.
    LM_ONED_FAST_SCAN = 0x100
    #Reserved setting for localization mode.
    LM_REV = -2147483648
    #Skips localization. 
    LM_SKIP = 0x00
}
```
