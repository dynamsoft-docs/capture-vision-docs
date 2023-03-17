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

| BarcodeFilteringCondition | Description |
| ------------------------- | ----------- |
| [`ReferenceTargetROIDefNameArray`](#referencetargetroidefnamearray) | Set the names of `TargetROIDefOptions` that can be used as reference objects. |
| [`AtomicResultTypeArray`](#atomicresulttypearray) | Set atomic result types that can be used as reference objects. |
| [`BarcodeFilteringCondition`](#barcodefilteringcondition) | Set barcode conditions that can be used as reference objects. |
| [`FrameFilteringCondition`](#framefilteringcondition) | Set frame conditions that can be used as reference objects. |
| [`TableCellFilteringCondition`](#tablecellfilteringcondition) | Set table cell conditions that can be used as reference objects |
| [`TextLineFilteringCondition`](#textlinefilteringcondition) | Set text line conditions that can be used as reference objects |
| [`ColourRegionFilteringCondition`](#colourregionfilteringcondition) | Set colour region conditions that can be used as reference objects |

| BarcodeFilteringCondition Parameters | Description |
| ------------------------------------ | ----------- |
| [`BarcodeFormatIds`](#barcodeformatids) | Filter the barcode by barcode format ID. |
| [`BarcodeTextRegExPattern`](#barcodetextregexpattern) | Filter the barcode by barcode text. |

| FrameFilteringCondition Parameters | Description |
| ---------------------------------- | ----------- |
| [`ImageDimensionRange`](#imagedimensionrange) |  |
| [`AspectRatioRange`](#aspectratiorange) |  |
| [`WidthRange`](#widthrange) |  |
| [`HeightRange`](#heightrange) |  |

| TableCellFilteringCondition Parameters | Description |
| -------------------------------------- | ----------- |
| [`RowNumbers`](#rownumbers) |  |
| [`ColNumbers`](#colnumbers) |  |

| TextLineFilteringCondition Parameters | Description |
| -------------------------------------- | ----------- |
| [`LineNumbers`](#linenumbers) |  |
| [`LineStringRegExPattern`](#linestringregexpattern) |  |

| ColourRegionFilteringCondition Parameters | Description |
| ----------------------------------------- | ----------- |
| [`RegionPredetectionMode`](#regionpredetectionmode) |  |
| [`ImageDimensionRange`](#imagedimensionrange-1) |  |
| [`AspectRatioRange`](#aspectratiorange-1) |  |
| [`WidthRange`](#widthrange-1) |  |
| [`HeightRange`](#heightrange-1) |  |

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
