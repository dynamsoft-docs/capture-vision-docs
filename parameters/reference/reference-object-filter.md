---
layout: default-layout
title: ReferenceObjectFilter of TargetROIDefOption
description:
keywords:
needAutoGenerateSidebar: true
breadcrumbText:
---

# ReferenceObjectFilter

Set a series of filter conditions for the reference objects. A reference object is picked from the intermediate results that previously captured by the library. In the parameter ReferenceObjectFilter, you can add conditions to filter which intermediate results can be use as reference objects. If `ReferenceObjectFilter` is not set, the whole image will be treated as the reference object.

```json
{
    //...
    "ReferenceObjectFilter" :
    {
        "ReferenceTargetROIDefNameArray": ["TR_0", "TR_1"], 
        "AtomicResultTypeArray" : ["ART_TEXT_LINE","ART_BARCODE","ART_FRAME","ART_TABLE_CELL"], 
        "BarcodeFilteringCondition": {},
        "FrameFilteringCondition": {},
        "TableCellFilteringCondition": {},
        "TextLineFilteringCondition": {},
        "ColourRegionFilteringCondition": {}
    },
    //...
}
```

## ReferenceObjectFilter Parameters Summary

| ReferenceObjectFilter Parameters | Description | Type | Range | Default Value |
| -------------------------------- | ----------- | ---- | ----- | ------------- |
| [`ReferenceTargetROIDefNameArray`](#referencetargetroidefnamearray) | Filter the reference object by specifying the names of `TargetROIDefOptions`. | *Array* |  | null |
| [`AtomicResultTypeArray`](#atomicresulttypearray) | Set atomic result types that can be used as reference objects. | *Array* | Each array element should be one of the `AtomicResultType`. | ["ART_TEXT_LINE","ART_BARCODE","ART_TABLE_CELL", "ART_FRAME"] |
| [`BarcodeFilteringCondition`](#barcodefilteringcondition) | Set barcode conditions that can be used as reference objects. | *Object* |  | null |
| [`FrameFilteringCondition`](#framefilteringcondition) | Set frame conditions that can be used as reference objects. | *Object* |  | null |
| [`TableCellFilteringCondition`](#tablecellfilteringcondition) | Set table cell conditions that can be used as reference objects | *Object* |  | null |
| [`TextLineFilteringCondition`](#textlinefilteringcondition) | Set text line conditions that can be used as reference objects | *Object* |  | null |
| [`ColourRegionFilteringCondition`](#colourregionfilteringcondition) | Set colour region conditions that can be used as reference *objects* | *Object* |  | null |

| BarcodeFilteringCondition Parameters | Description | Default Value |
| ------------------------------------ | ----------- | ------------- |
| [`BarcodeFormatIds`](#barcodeformatids) | Specify a group of `BarcodeFormatIds` with a string array as the filter condition. | ["BF_ALL"] |
| [`BarcodeTextRegExPattern`](#barcodetextregexpattern) | Find qualified barcode reference objects by settings a RegEx string for the barcode text. | null |

| FrameFilteringCondition Parameters | Description | Default Value |
| ---------------------------------- | ----------- | ------------- |
| [`ImageDimensionRange`](#imagedimensionrange) | Set an int array as the image dimension range to filter the source image. | [16384,0x7fffffff] |
| [`AspectRatioRange`](#aspectratiorange) | Set an int array as the aspect ratio range to filter the source image. | [1, 10000] |
| [`WidthRange`](#widthrange) | Set an int array as the width range to filter the source image. | [1, 0x7fffffff] |
| [`HeightRange`](#heightrange) | Set an int array as the height range to filter the source image. | [1, 0x7fffffff] |

| TableCellFilteringCondition Parameters | Description | Default Value |
| -------------------------------------- | ----------- | ------------- |
| [`RowNumbers`](#rownumbers) | Set a group of row numbers with a string to specify which table cells to reference. | null |
| [`ColNumbers`](#colnumbers) | Set a group of column numbers with a string to specify which table cells to reference. | null |

| TextLineFilteringCondition Parameters | Description | Default Value |
| ------------------------------------- | ----------- | ------------- |
| [`LineNumbers`](#linenumbers) | Set a group of line numbers with a string to specify which lines to reference. | null |
| [`LineStringRegExPattern`](#linestringregexpattern) | Set a RegEx string as the rule to filter the text line content. | null |

| ColourRegionFilteringCondition Parameters | Description | Default Value |
| ----------------------------------------- | ----------- | ------------- |
| [`RegionPredetectionMode`](#regionpredetectionmode) | Filter the region of predetection ressults by their modes. | null |
| [`ImageDimensionRange`](#imagedimensionrange-1) | Set an int array as the image dimension range to filter the predetected region. | null |
| [`AspectRatioRange`](#aspectratiorange-1) | Set an int array as the aspect ratio range to filter the predetected region. | null |
| [`WidthRange`](#widthrange-1) | Set an int array as the width range to filter the predetected region. | null |
| [`HeightRange`](#heightrange-1) | Set an int array as the height range to filter the predetected region. | null |

## ReferenceObjectFilter Parameters Details

### ReferenceTargetROIDefNameArray

Set the names of `TargetROIDefOptions` that can be used as reference objects.

**Default Value**

[]

**Range**

N/A

&nbsp;

### AtomicResultTypeArray

Set atomic result types that can be used as reference objects.

**Default Value**

["ART_TEXT_LINE","ART_BARCODE","ART_TABLE_CELL", "ART_FRAME"]

**Range**

Each array element of `AtomicResultTypeArray` can be one of the `AtomicResultType` which are:

- ART_TEXT_LINE
- ART_BARCODE
- ART_FRAME
- ART_TABLE_CELL
- ART_GEOMETRY_LINE
- ART_CORNER
- ART_COLOUR_REGION"

&nbsp;

### BarcodeFilteringCondition

Filter the reference objects by the decoded barcodes information. Barcode filtering is not implemented by default.

#### BarcodeFormatIds

Filter the barcode by barcode format ID.

**Default Value**

["BF_ALL"]

**Range**

An array of `BarcodeFormatIds`.

#### BarcodeTextRegExPattern

Filter the barcode by barcode text.

**Default Value**

""

**Range**

N/A

&nbsp;

### FrameFilteringCondition

Filter the reference objects by the frame information. Barcode filtering is not implemented by default.

#### ImageDimensionRange

**Description**

**Default Value**

**Range**

#### AspectRatioRange

**Description**

**Default Value**

**Range**

#### WidthRange

**Description**

**Default Value**

**Range**

#### HeightRange

**Description**

**Default Value**

**Range**

&nbsp;

### TableCellFilteringCondition

#### RowNumbers

**Description**

**Default Value**

**Range**

#### ColNumbers

**Description**

**Default Value**

**Range**

#### RegionState

**Description**

**Default Value**

**Range**

&nbsp;

### TextLineFilteringCondition

#### LineNumbers

**Description**

**Default Value**

**Range**

#### LineStringRegExPattern

**Description**

**Default Value**

**Range**

#### RegionState

**Description**

**Default Value**

**Range**

&nbsp;

### ColourRegionFilteringCondition

#### RegionPredetectionMode

**Description**

**Default Value**

**Range**

#### ImageDimensionRange

**Description**

**Default Value**

**Range**

#### AspectRatioRange

**Description**

**Default Value**

**Range**

#### WidthRange

**Description**

**Default Value**

**Range**

#### HeightRange

**Description**

**Default Value**

**Range**
