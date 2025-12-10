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
| `Name`           | Represents the name of the ImageSource object, which serves as its unique identifier.                    |
| `Type`           | Indicates the type of the `ImageSource` object, which helps CVR create the correct type of image source. |
| `DirectoryPath`  | Specifies a local directory, the files within which are fetched as images to process.                    |
| `FileFilter`     | Specifies a file name filter string, which determines which files are fetched.                           |
| `Recursive`      | Indicates whether to fetch files recursively.                                                            |
| `PDFReadingMode` | Defines how to handle PDF files.                                                                         |
| `Pages`          | Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching.                                                                         |


### Sub Parameters of PDFReadingMode 

| Parameter Name | Description                                                                                           |
| -------------- | ----------------------------------------------------------------------------------------------------- |
| `Mode`         | Specifies the operation mode. Read more about [PDFReadingMode](../../enums/core/pdf-reading-mode.md). |
| `DPI`          | Specifies the DPI used when rasterizing a PDF into images.                                            |
| `TargetType`   | Specifies a the target type. Read more about [TargetType](../../enums/core/target-type.md).           |