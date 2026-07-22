---
layout: default-layout
title: PDFReadingMode - Dynamsoft Capture Vision Parameters
description: Reference for the PDFReadingMode parameter in the Dynamsoft Capture Vision ImageSource object, which controls how PDF files are rendered into images, including the reading mode (raster/vector/auto), DPI, and raster data source.
keywords: PDF reading mode, ISA
---
# PDFReadingMode

Parameter `PDFReadingMode` defines how to handle PDF files.

## JSON Structure

**Location in template:**
```
ImageSourceOptions
    └── PdfReadingMode
```

**Parent object:** [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object

**Example:**

```json
{
    "PDFReadingMode":
    {
        "Mode": "PDFRM_RASTER",
        "DPI": 300,
        "RasterDataSource": "RDS_RASTERIZED_PAGES"
    }
}
```

> [!NOTE]
> - This snippet shows only the `PdfReadingMode` parameter.
> - To use it, embed this parameter within a [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

Parameter `PDFReadingMode` is configured by a PDF reading mode objects. The PDF reading mode object includes a candidate mode and a series of mode arguments. The available mode arguments of the PDF reading mode object is shown as follow.

### Mode Arguments

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Mode Argument Name</th>
            <th nowrap="nowrap">Mode Argument Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Mode</td>
        <td><b>Description</b><br>Specifies the operation mode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>PDFRM_VECTOR<br>PDFRM_RASTER
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">DPI</td>
        <td><b>Description</b><br>Specifies the DPI used when rasterizing a PDF into images.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[100,3000]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>300
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>The resolution of the rendered image is calculated as follows:<br>Set PDF page height to h and page width to w,<br>Final rendered image height  ImgHeight = h / 72 * DPI<br>Final rendered image width  ImgWidth = w / 72 * DPI<br>DPI is the number of pixels per inch of the image.<br>The page width and height unit defined in PDF is pt (length unit, 1 inch = 72 pt), so in the above formula we first divide the width and height by 72 to get the inch length of the page, and then multiply by DPI to get the final image pixel width and height.
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">RasterDataSource</td>
        <td><b>Description</b><br>Specifies a the target type.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the candidate mode as a string<br>RDS_RASTERIZED_PAGES<br>RDS_EXTRACTED_IMAGES
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>RDS_RASTERIZED_PAGES
        </td>
    </tr>
</table>

### Default Setting

If the `PDFReadingMode` is not configured in your template file, the following settings will be used as the default setting.

```json
{
    "PDFReadingMode": 
    {
        "Mode": "PDFRM_RASTER",
        "DPI": 300,
        "RasterDataSource": "RDS_RASTERIZED_PAGES"
    }
}
```

## Candidate Mode Introduction

### PDFRM_RASTER

Renders each page of the PDF as an image, which will be processed later. This reading mode can be used for all PDF files, but the drawback is that you need to choose the appropriate value of PDFRasterDPI to render the image. Otherwise, if the image is too large, the processing speed of DBR may be slowed, and if the image is too small, the barcode region may be distorted and cannot be decoded.

### PDFRM_VECTOR

This mode will not render PDF data into images, but directly extract PDF vector data for barcode region positioning and decoding. This mode can offer faster speed and higher accuracy, but it is only suitable for PDF composed of vector data.
