---
layout: default-layout
title: ImageSourceOptions Parameters - Dynamsoft Capture Vision
description: Reference index for ImageSourceOption object in Dynamsoft Capture Vision parameters, which configure image input sources such as directories, scanners, and cameras.
keywords: ImageSourceOptions, image source, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# ImageSourceOption Parameters

The `ImageSourceOption` object defines the input source for Dynamsoft Capture Vision, including image directories, scanners, cameras, and other sources.

## Example JSON

```json
{
    "ImageSourceOptions": [
        {
            "Name": "DirectoryFetcher_0",
            "Type": "IST_DIRECTORY_FETCHER",
            "DirectoryPath": "C:\\Users\\Admin\\Pictures\\",
            "FileFilter": "",
            "Recursive": 1,
            "PDFReadingMode": {
                "Mode": "PDFRM_RASTER",
                "DPI": 300,
                "TargetType": "TT_PAGE"
            },
            "Pages": [0, 3, 5, 7, 10]
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `ImageSourceOptions` object inside `ImageSourceOptions`.

```text
ImageSourceOption
├── Name
├── Type
├── DirectoryPath
├── FileFilter
├── Recursive
├── PDFReadingMode
└── Pages
```

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the `ImageSourceOption` object. |
| [`Type`](type.md) | The type of image source. |
| [`DirectoryPath`](directory-path.md) | The path to the image directory. |
| [`FileFilter`](file-filter.md) | The file filter for selecting images. |
| [`Recursive`](recursive.md) | Whether to search subdirectories recursively. |
| [`PDFReadingMode`](pdf-reading-mode.md) | The mode for reading PDF files. |
| [`Pages`](pages.md) | The pages to process from multi-page files. |


