---
layout: default-layout
Title: ModuleSizeRangeArray - Dynamsoft Barcode Reader Parameters
Description: The parameter ModuleSizeRangeArray of Dynamsoft Barcode Reader defines the range of module size (in pixels) while barcode searching and result filtering.
Keywords: ModuleSizeRangeArray , parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/module-size-range-array.html
---

# ModuleSizeRangeArray

Parameter `ModuleSizeRangeArray` defines the range of module size (in pixels) while barcode searching and result filtering.

## Example

```json
{
    "ModuleSizeRangeArray": 
    [
        {
            "MinValue": 3,
            "MaxValue": 20
        }
    ]
}
```

## Parameter Summary

Parameter `ModuleSizeRangeArray` consist of a group of barcode module size range objects. Each barcode angle range object includes the maximum and minimum value of the barcode module size range.

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MinValue<br></td>
        <td><b>Description</b><br>Defines the MinValue of the barcode module size range.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">MaxValue<br></td>
        <td><b>Description</b><br>Defines the MaxValue of the barcode module size range.</td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i></td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,0x7fffffff]
        </td>
    </tr>
</table>

### Default Settings

If the `ModuleSizeRangeArray` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "ModuleSizeRangeArray": []
}
```
