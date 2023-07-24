---
layout: default-layout
Title: PDFReadingMode - Dynamsoft Core Enumerations
Description: The enumeration PDFReadingMode of Dynamsoft Core describes all available PDF reading modes.
Keywords: PDF Reading Mode
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: PDFReadingMode
---

# Enumeration PDFReadingMode

`PDFReadingMode` describes the PDF reading modes.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
export enum EnumPDFReadingMode
{
   /** Outputs vector data found in the PDFs.*/
   PDFRM_VECTOR = 1,
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, 
    * the SDK may rasterize the PDF pages.
    * Check the template for available argument settings.*/
   PDFRM_RASTER = 2,
   /** Reserved setting for PDF reading mode.*/
   PDFRM_REV = -2147483648
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumPDFReadingMode
{
   /** Capture content from vector data in PDF file. */
   public static final int PDFRM_VECTOR = 1;
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   public static final int PDFRM_RASTER = 2;
   /** Reserved setting for PDF reading mode.*/
   public static final int PDFRM_REV = -2147483648;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSPDFReadingMode)
{
   /** Capture content from vector data in PDF file. */
   DSPDFReadingModeVector = 0x01,
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   DSPDFReadingModeRaster = 0x02,
   /** Reserved setting for PDF reading mode.*/
   DSPDFReadingModeRev = -2147483648
};
```
>
```swift
public enum PDFReadingMode : Int
{
   /** Capture content from vector data in PDF file. */
   vector = 0x01,
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   raster = 0x02,
   /** Reserved setting for PDF reading mode.*/
   rev = -2147483648
};
```
>
```cpp
typedef enum PDFReadingMode
{
   /** Outputs vector data found in the PDFs. */
   PDFRM_VECTOR = 0x01,
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   PDFRM_RASTER = 0x02,
   /** Reserved setting for PDF reading mode.*/
#if defined(_WIN32) || defined(_WIN64)
   PDFRM_REV = 0x80000000,
#else
   PDFRM_REV = -2147483648,
#endif
} PDFReadingMode;
```
