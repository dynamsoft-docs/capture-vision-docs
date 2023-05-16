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
```
>
```java
```
>
```objc
```
>
```swift
```
>
```cpp
typedef enum PDFReadingMode
{
   /** Outputs vector data found in the PDFs. */
   PDFRM_VECTOR = 0x01,
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, 
    * the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   PDFRM_RASTER = 0x02,   
   /** Reserved setting for PDF reading mode. */
#if defined(_WIN32) || defined(_WIN64)
   PDFRM_REV = 0x80000000,
#else
   PDFRM_REV = -2147483648,
#endif
} PDFReadingMode;
```
