---
layout: default-layout
Title: SectionImageParameterArray - Dynamsoft Capture Vision Shared Parameters
Description: The parameter SectionImageParameterArray defines the image processing algorithms that implemented in the different sections of an algorithm task.
Keywords: Section image parameter
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/shared-parameter/section-image-parameter-array.html
---

# SectionImageParameterArray

Parameter `SectionImageParameterArray` defines the image processing algorithms that implemented in the task. Each member of the array defines an algorithm section as well as its image processing parameters.

## Example

```json
{
    "SectionImageParameterArray":
    [
        {
            "Section": "REGION_PREDETECTION",
            "ImageParameterName": "IP_0"
        },
        {
            "Section": "TEXT_LINE_LOCALIZATION",
            "ImageParameterName": "IP_1"
        }

    ]
}
```

## Parameter Summary

Note: Parameter `SectionImageParameterArray` is available for  `BarcodeReaderTaskSetting`, `LabelRecognizerTaskSetting` and `DocumentNormalizerTaskSetting`. It has different parameter range and default value under different parent object.

### As a BarcodeReaderTaskSetting Parameter

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
        <td><b>Range</b><br>One of the following <b>SectionType</b> as a string.<br>ST_REGION_PREDETECTION
        <br>ST_BARCODE_LOCALIZATION
        <br>ST_BARCODE_DECODING
        </td>
    </tr>
    <tr>
        <td rowspan = "2" style="vertical-align:text-top">ImageParameterName<br></td>
        <td><b>Description</b><br>Specifies a name that defined under ImageParameterOptions.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
</table>

### As a DocumentNormalizerTaskSetting Parameter

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
                <br>ST_DOCUMENT_DETECTION
                <br>ST_DOCUMENT_NORMALIZATION
        </td>
    </tr>
    <tr>
        <td rowspan = "2" style="vertical-align:text-top">ImageParameterName<br></td>
        <td><b>Description</b><br>Specifies a name that defined under ImageParameterOptions.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
</table>

### As a LabelRecognizerTaskSetting Parameter

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
        <td><b>Description</b><br>Specifies a name that defined under ImageParameterOptions.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
</table>
