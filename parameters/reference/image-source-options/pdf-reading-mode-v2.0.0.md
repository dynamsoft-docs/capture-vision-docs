---
layout: default-layout
title: PDFReadingMode - Dynamsoft Capture Vision Parameters
description: The parameter PDFReadingMode of Dynamsoft Capture Vision defines .
keywords: PDF reading mode, ISA
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/image-source-options/pdf-reading-mode-v2.0.0.html
---

# PDFReadingMode

Parameter `PDFReadingMode` defines how to handle PDF files.

## Example

```json
{
    "PDFReadingMode": 
    {
        "Mode": "PDFRM_RASTER",
        "DPI": 300,
        "TargetType": "TT_PAGE"
    }
}
```

## Parameter Summary

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
        <td rowspan = "4" style="vertical-align:text-top">DPI</td>
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
        <td rowspan = "4" style="vertical-align:text-top">TargetType</td>
        <td><b>Description</b><br>Specifies a the target type.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the candidate mode as a string</b><br>TT_PAGE<br>TT_IMAGE
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>TT_PAGE
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
        "TargetType": "TT_PAGE"
    }
}
```

## Candidate Mode Introduction

### PDFRM_RASTER

Converts the PDF file to image(s) first, then detects barcode

### PDFRM_VECTOR

Detects barcode from vector data in PDF file.
