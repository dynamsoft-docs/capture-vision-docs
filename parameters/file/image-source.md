---   
layout: default-layout
title: ImageSource - Dynamsoft Capture Vision Parameters
description: The ImageSource object in the Dynamsoft Capture Vision Settings File.
keywords: ImageSource
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Design of the ImageSource Object

An `ImageSource` object defines an image source to be created and maintained by Capture Vision Router (CVR).

```json
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
    "Pages": [0,3,5,7,10]
}
```


## Summary of ImageSource top-level parameters

| Parameter Name   | Description                                                                                              |
| ---------------- | -------------------------------------------------------------------------------------------------------- |
| [`Name`]({{ site.dcvb_parameters_reference }}image-source-options/name.html)           | Represents the name of the `ImageSource` object, which serves as its unique identifier.                    |
| [`Type`]({{ site.dcvb_parameters_reference }}image-source-options/type.html)           | Indicates the type of the `ImageSource` object, which helps CVR create the correct type of image source. |
| [`DirectoryPath`]({{ site.dcvb_parameters_reference }}image-source-options/directory-path.html)  | Specifies a local directory, the files within which are fetched as images to process.                    |
| [`FileFilter`]({{ site.dcvb_parameters_reference }}image-source-options/file-filter.html)     | Specifies a file name filter string, which determines which files are fetched.                           |
| [`Recursive`]({{ site.dcvb_parameters_reference }}image-source-options/recursive.html)      | Indicates whether to fetch files recursively.                                                            |
| [`PDFReadingMode`]({{ site.dcvb_parameters_reference }}image-source-options/pdf-reading-mode.html) | Defines how to handle PDF files.                                                                         |
| [`Pages`]({{ site.dcvb_parameters_reference }}image-source-options/pages.html)          | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |

