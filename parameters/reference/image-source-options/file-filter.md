---
layout: default-layout
title: FileFilter - Dynamsoft Capture Vision Parameters
description: The parameter FileFilter of Dynamsoft Capture Vision defines .
keywords: File filter, ISA
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/image-source-options/file-filter.html
---

# FileFilter

Parameter `FileFilter` specifies a file name filter string, which determines which files are fetched.

## Example

```json
{
    "FileFilter": "*.JPG"
}
```

## Parameter Summary

| ScaleDownThreshold Parameter Summary |
| :----------------------------------- |
| **Description**<br>A file name filter string |
| **Type**<br>*String* |
| **Value range**<br>One of the files extension name. For example: "\*.BMP;\*.JPG;\*.GIF", or "\*.\*", etc. |
| **Default Value**<br>"" |
