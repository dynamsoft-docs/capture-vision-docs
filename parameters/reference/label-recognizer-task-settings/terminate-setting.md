---
layout: default-layout
title: TerminateSetting - Dynamsoft Label Recognizer Parameters
description: The parameter TerminateSetting defines the terminate stages of the label recognition task.
keywords: Terminate setting
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/label-recognizer-task-settings/terminate-setting.html
---

# TerminateSetting

Parameter `TerminateSetting` defines the terminate stages of each section in the task. For each sections, you can define only one terminate stage.

## Example

```json
"TerminateSetting":
{
    "Section": "ST_REGION_PREDETECTION",
    "Stage": "IRUT_GRAYSCALE_IMAGE"
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
        <td><b>Description</b><br>Specifies a mode for ordering.</td>
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
| ST_REGION_PREDETECTION | IRUT_COLOUR_IMAGE<br>IRUT_SCALED_DOWN_COLOUR_IMAGE<br>IRUT_GRAYSCALE_IMAGE<br>IRUT_TRANSFORMED_GRAYSCALE_IMAGE<br>IRUT_PREDETECTED_REGIONS |
| ST_TEXT_LINE_LOCALIZATION | IRUT_COLOUR_IMAGE<br>IRUT_SCALED_DOWN_COLOUR_IMAGE<br>IRUT_GRAYSCALE_IMAGE<br>IRUT_TRANSFORMED_GRAYSCALE_IMAGE<br>IRUT_ENHANCED_GRAYSCALE_IMAGE<br>IRUT_BINARY_IMAGE<br>IRUT_TEXTURE_DETECTION_RESULT<br>IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE<br>IRUT_TEXTURE_REMOVED_BINARY_IMAGE<br>IRUT_TEXT_ZONES<br>IRUT_TEXT_REMOVED_BINARY_IMAGE<br>IRUT_LOCALIZED_TEXT_LINES |
| ST_TEXT_LINE_RECOGNITION | IRUT_COLOUR_IMAGE<br>IRUT_GRAYSCALE_IMAGE<br>IRUT_TRANSFORMED_GRAYSCALE_IMAGE<br>IRUT_RECOGNIZED_TEXT_LINES |
