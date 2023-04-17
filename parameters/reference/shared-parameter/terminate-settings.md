---
layout: default-layout
Title: StartSection - Dynamsoft Capture Vision Shared Parameters
Description: The parameter StartSection defines the terminate stages of the task.
Keywords: Max threads
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TerminateSetting

Parameter `StartSection` defines the terminate stages of the task. For each sections in an alogrithm task, you can define only one terminate stage.

```json
"TerminateSetting":
{
    "Section": "ST_REGION_PREDETECTION",
    "Stage": "IRUT_GRAYSCALE_IMAGE"
}
```

## As a BarcodeReaderTaskSetting Parameter

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Section<br></td>
        <td><b>Description</b><br>Specifies a mode for ordering.</td>
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
        <td rowspan = "3" style="vertical-align:text-top">Stage<br></td>
        <td><b>Description</b><br>Specifies a mode for ordering.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the <b>IntermediateResultUnitType</b> as a string. The available stage type is different for each sections. View the <a href="#appendix---available-stage-for-sections">appendix</a> for more details.
        </td>
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
        <td><b>Description</b><br>Specifies a mode for ordering.</td>
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
        <td rowspan = "3" style="vertical-align:text-top">Stage<br></td>
        <td><b>Description</b><br>Specifies a mode for ordering.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the <b>IntermediateResultUnitType</b> as a string. The available stage type is different for each sections. View the <a href="#appendix---available-stage-for-sections">appendix</a> for more details.
        </td>
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
        <td><b>Description</b><br>Specifies a mode for ordering.</td>
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
        <td rowspan = "3" style="vertical-align:text-top">Stage<br></td>
        <td><b>Description</b><br>Specifies a mode for ordering.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the <b>IntermediateResultUnitType</b> as a string. The available stage type is different for each sections. View the <a href="#appendix---available-stage-for-sections">appendix</a> for more details.
        </td>
    </tr>
</table>

## Appendix - Available Stage for Sections

| Section             | Available Stages |
| :------------------ | :--------------- |
| ST_REGION_PREDETECTION | <li>IRUT_COLOUR_IMAGE</li><li>IRUT_SCALED_DOWN_COLOUR_IMAGE</li><li>IRUT_GRAYSCALE_IMAGE</li><li>IRUT_TRANSFORMED_GRAYSCALE_IMAGE</li><li>IRUT_PREDETECTED_REGIONS</li> |
| ST_BARCODE_LOCALIZATION | <li>IRUT_COLOUR_IMAGE</li><li>IRUT_SCALED_DOWN_COLOUR_IMAGE</li><li>IRUT_GRAYSCALE_IMAGE</li><li>IRUT_TRANSFORMED_GRAYSCALE_IMAGE</li><li>IRUT_ENHANCED_GRAYSCALE_IMAGE</li><li>IRUT_BINARY_IMAGE</li><li>IRUT_TEXTURE_DETECTION_RESULT</li><li>IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE</li><li>IRUT_TEXTURE_REMOVED_BINARY_IMAGE</li><li>IRUT_TEXT_ZONES</li><li>IRUT_TEXT_REMOVED_BINARY_IMAGE <li>IRUT_CONTOURS</li><li>IRUT_LINE_SEGMENTS</li><li>IRUT_CANDIDATE_BARCODE_ZONES</li><li>IRUT_LOCALIZED_BARCODES |
| ST_BARCODE_DECODING | <li>IRUT_COLOUR_IMAGE</li><li>IRUT_GRAYSCALE_IMAGE</li><li>IRUT_TRANSFORMED_GRAYSCALE_IMAGE</li><li>IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE</li><li>IRUT_COMPLEMENTED_BARCODE_IMAGE</li><li>IRUT_SCALED_UP_BARCODE_IMAGE</li><li>IRUT_DECODED_BARCODES |
| ST_DOCUMENT_DETECTION | <li>IRUT_COLOUR_IMAGE</li><li>IRUT_SCALED_DOWN_COLOUR_IMAGE</li><li>IRUT_GRAYSCALE_IMAGE</li><li>IRUT_TRANSFORMED_GRAYSCALE_IMAGE</li><li>IRUT_ENHANCED_GRAYSCALE_IMAGE</li><li>IRUT_BINARY_IMAGE</li><li>IRUT_TEXTURE_DETECTION_RESULT</li><li>IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE</li><li>IRUT_TEXTURE_REMOVED_BINARY_IMAGE</li><li>IRUT_TEXT_ZONES</li><li>IRUT_TEXT_REMOVED_BINARY_IMAGE</li><li>IRUT_CONTOURS</li><li>IRUT_LINE_SEGMENTS</li><li>IRUT_LONG_LINES</li><li>IRUT_CORNERS</li><li>IRUT_CANDIDATE_QUAD_EDGES</li><li>IRUT_DETECTED_QUADS |
| ST_DOCUMENT_NORMALIZATION | <li>IRUT_NORMALIZED_IMAGE</li> |
| ST_TEXT_LINE_LOCALIZATION | <li>IRUT_COLOUR_IMAGE</li><li>IRUT_SCALED_DOWN_COLOUR_IMAGE</li><li>IRUT_GRAYSCALE_IMAGE</li><li>IRUT_TRANSFORMED_GRAYSCALE_IMAGE</li><li>IRUT_ENHANCED_GRAYSCALE_IMAGE</li><li>IRUT_BINARY_IMAGE</li><li>IRUT_TEXTURE_DETECTION_RESULT</li><li>IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE</li><li>IRUT_TEXTURE_REMOVED_BINARY_IMAGE</li><li>IRUT_TEXT_ZONES</li><li>IRUT_TEXT_REMOVED_BINARY_IMAGE</li><li>IRUT_LOCALIZED_TEXT_LINES</li> |
| ST_TEXT_LINE_RECOGNITION | <li>IRUT_COLOUR_IMAGE</li><li>IRUT_GRAYSCALE_IMAGE</li><li>IRUT_TRANSFORMED_GRAYSCALE_IMAGE</li><li>IRUT_RECOGNIZED_TEXT_LINES</li> |
