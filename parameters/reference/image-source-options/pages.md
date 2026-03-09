---
layout: default-layout
title: Pages - Dynamsoft Capture Vision Parameters
description: Reference for the Pages parameter in the Dynamsoft Capture Vision ImageSource object, which sets the 0-based page indexes of a multi-page file (PDF or TIFF) to be processed.
keywords: Pages, ISA
needGenerateH3Content: true
---
# Pages

Parameter `Pages` sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching.

## JSON Structure

**Location in template:**
```
ImageSourceOptions
    └── Pages
```

**Parent object:** [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object

**Example:**

```json
{
    "Pages": [0,3,5,7,10]
}
```

> [!NOTE]
> - This snippet shows only the `Pages` parameter.
> - To use it, embed this parameter within a [ImageSource]({{ site.dcvb_parameters }}file/image-source.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Pages Parameter Details |
| :--------------------- |
| **Description**<br>Sets the 0-based page indexes of a file (.tiff or .pdf) for barcode searching. |
| **Type**<br>*int array* |
| **Value range**<br>Each array item represents a specified 0-based page index. |
