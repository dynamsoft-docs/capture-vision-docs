---
layout: default-layout
title: RasterDataSource - Dynamsoft Core Enumerations
description: The enumeration RasterDataSource of Dynamsoft Core describes raster data source types.
keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RasterDataSource
---

# Enumeration RasterDataSource

`RasterDataSource` describes the target types.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
export enum EnumRasterDataSource
{
   /**The raster data source type of the PDF file is "pages". Only available for PDFReadingMode PDFRM_RASTER.*/
   RDS_RASTERIZED_PAGES = 0,
   /**The raster data source type of the PDF file is "images".*/
   RDS_EXTRACTED_IMAGES = 1
}
```
>
```java
public @interface EnumRasterDataSource {
   /**The raster data source type of the PDF file is "pages". Only available for PDFReadingMode raster.*/
   public static final int RDS_RASTERIZED_PAGES = 0;
   /**The raster data source type of the PDF file is "images".*/
   public static final int RDS_EXTRACTED_IMAGES = 1;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSRasterDataSource)
{
   /**The raster data source type of the PDF file is "pages". Only available for PDFReadingMode raster.*/
   DSRasterDataSourceRasterizedPages = 0,
   /**The raster data source type of the PDF file is "images".*/
   DSRasterDataSourceExtractedImages = 1
}NS_SWIFT_NAME(RasterDataSource);
```
>
```swift
public enum RasterDataSource : Int
{
   /**The raster data source type of the PDF file is "pages". Only available for PDFReadingMode raster.*/
   rasterizedPages = 0,
   /**The raster data source type of the PDF file is "images".*/
   extractedImages = 1
}
```
>
```cpp
typedef enum RasterDataSource
{
   /**The raster data source type of the PDF file is "pages". Only available for PDFReadingMode PDFRM_RASTER.*/
   RDS_RASTERIZED_PAGES,
   /**The raster data source type of the PDF file is "images".*/
   RDS_EXTRACTED_IMAGES
} RasterDataSource;
```
