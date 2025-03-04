---
layout: default-layout
title: SectionImageParameterArray - Dynamsoft Label Recognizer Parameters
description: The parameter SectionImageParameterArray defines the image processing algorithms that implemented in the different sections of a label recognition algorithm task.
keywords: Section image parameter
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# SectionImageParameterArray

`SectionImageParameterArray` is a parameter that defines `ImageParameter` in section unit. Each `SectionImageParameterArray` element is a group of a section name and a `ImageParameter` name so that this section will use the ImageParameter you specified. If a section is not specified in the array, it will use the default `ImageParameter` configuration.

The `LabelRecognizerTask` includes the following sections:

* `ST_REGION_PREDETECTION`
* `ST_TEXT_LINE_LOCALIZATION`
* `ST_TEXT_LINE_RECOGNITION`

## Example

```json
{
    "SectionImageParameterArray":
    [
        {
            "Section": "ST_REGION_PREDETECTION",
            "ImageParameterName": "IP_0"
        },
        {
            "Section": "ST_TEXT_LINE_LOCALIZATION",
            "ImageParameterName": "IP_1"
        },
        {
            "Section": "ST_TEXT_LINE_RECOGNITION",
            "ImageParameterName": "IP_1"
        }
    ]
}
```

## Parameter Summary

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Section<br></td>
        <td><b>Description</b><br>Specifies an algorithm section.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the following <b>SectionType</b> as a string.
                <br>ST_REGION_PREDETECTION
                <br>ST_TEXT_LINE_LOCALIZATION
                <br>ST_TEXT_LINE_RECOGNITION
        </td>
    </tr>
    <tr>
        <td rowspan = "2" style="vertical-align:text-top">ImageParameterName<br></td>
        <td><b>Description</b><br>Specifies the ImageParameter that you want to implement in this section. It must be one of the name that defined under ImageParameterOptions.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
</table>
