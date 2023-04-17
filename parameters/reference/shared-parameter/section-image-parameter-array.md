---
layout: default-layout
Title: SectionImageParameterArray - Dynamsoft Capture Vision Shared Parameters
Description: The parameter SectionImageParameterArray defines the image processing algorithms that implemented in the different sections of an algorithm task.
Keywords: Max threads
needAutoGenerateSidebar: true
noTitleIndex: true
---

# SectionImageParameterArray

`SectionImageParameterArray` is the parameter for you to set the image processing algorithms that implemented in the task. Each member of the array defines an algorithm section as well as its image processing parameters.

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

> Note: Parameter `SectionImageParameterArray` is available for  `BarcodeReaderTaskSetting`, `LabelRecognizerTaskSetting` and `DocumentNormalizerTaskSetting`. They have different parameter range and default value.

## As a BarcodeReaderTaskSetting Parameter

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Section<br></td>
        <td><b>Description</b><br>Specifies an algorithm section.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the following <b>SectionType</b> as a string.
            <ul>
                <li>ST_REGION_PREDETECTION</li>
                <li>ST_BARCODE_LOCALIZATION</li>
                <li>ST_BARCODE_DECODING</li>
            </ul>
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

## As a DocumentNormalizerTaskSetting Parameter

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Section<br></td>
        <td><b>Description</b><br>Specifies an algorithm section.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the following <b>SectionType</b> as a string.
            <ul>
                <li>ST_REGION_PREDETECTION</li>
                <li>ST_DOCUMENT_DETECTION</li>
                <li>ST_DOCUMENT_NORMALIZATION</li>
            </ul>
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

## As a LabelRecognizerTaskSetting Parameter

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Section<br></td>
        <td><b>Description</b><br>Specifies an algorithm section.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the following <b>SectionType</b> as a string.
            <ul>
                <li>ST_REGION_PREDETECTION</li>
                <li>ST_TEXT_LINE_LOCALIZATION</li>
                <li>ST_TEXT_LINE_RECOGNITION</li>
            </ul>
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
