---
layout: default-layout
Title: DeblurMode - Dynamsoft Barcode Reader Enumerations
Description: The enumeration DeblurMode of Dynamsoft Barcode Reader describes deblur modes that implemented on the localized barcodes.
Keywords: Deblur mode
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DeblurMode
---

# Enumeration DeblurMode

`DeblurMode` is implemented in the final stage of barcode decoding algorithm. It desides which image processing algorithms to perform on the localized barcode zones to extract the barcode information.

```cpp
typedef enum DeblurMode
{
    /** Performs deblur process using the direct binarization algorithm. */
    DM_DIRECT_BINARIZATION = 0x01,
    /** Performs deblur process using the threshold binarization algorithm. */
    DM_THRESHOLD_BINARIZATION = 0x02,
    /** Performs deblur process using the gray equalization algorithm. */
    DM_GRAY_EQUALIZATION = 0x04,
    /** Performs deblur process using the smoothing algorithm. */
    DM_SMOOTHING = 0x08,
    /** Performs deblur process using the morphing algorithm. */
    DM_MORPHING = 0x10,
    /** Performs deblur process using the deep analysis algorithm. */
    DM_DEEP_ANALYSIS = 0x20,
    /** Performs deblur process using the sharpening algorithm. */
    DM_SHARPENING = 0x40,
    /** Performs deblur process based on the binary image from the localization process. */
    DM_BASED_ON_LOC_BIN = 0x80,
    /** Performs deblur process using the sharpening and smoothing algorithm. */
    DM_SHARPENING_SMOOTHING = 0x100,
    /** Reserved setting for deblur mode. */
#if defined(_WIN32) || defined(_WIN64)
    DM_REV = 0x80000000,
#else
    DM_REV = -2147483648,
#endif
    /**Skips the deblur process. */
    DM_SKIP = 0x00
}DeblurMode;
```
