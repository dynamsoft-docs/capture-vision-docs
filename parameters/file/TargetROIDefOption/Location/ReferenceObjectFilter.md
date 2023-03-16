---
layout: default-layout
title: ReferenceObjectFilter of TargetROIDefOption
description:
keywords:
needAutoGenerateSidebar: true
breadcrumbText:
---

# ReferenceObjectFilter

Set filter conditions for the reference objects. If `ReferenceObjectFilter` is not set, the whole image will be treated as the reference object.

```json
{
    //...
    "Location": 
    {
        "ReferenceObjectFilter" :
        {  
            "ReferenceTargetROIDefNameArray": ["TR_0", "TR_1"], 
            "AtomicResultTypeArray" : ["ART_TEXT_LINE","ART_BARCODE","ART_FRAME","ART_TABLE_CELL"], 
            "BarcodeFilteringCondition": {},
            "FrameFilteringCondition": {},
            "TableCellFilteringCondition": {},
            "TextLineFilteringCondition": {},
            "ColourRegionFilteringCondition": {},
            "CornerFilteringCondition": {},
            "GeometryLineFilteringCondition": {},
        },
        //...
    },
    //...
}
```

What is reference object.
When to use this parameter

When it is hard to localize your target object but there are some other recognizable objects that can support your

How to use this Parameter

## ReferenceTargetROIDefNameArray

["TR_0", "TR_1"]
Optional, 默认[]，表示全图产生的结果均可以作为参考(排除自身)。

## AtomicResultTypeArray

Optional, ["ART_TEXT_LINE","ART_BARCODE","ART_TABLE_CELL", "ART_FRAME"]

"ART_TEXT_LINE","ART_BARCODE","ART_FRAME", "ART_TABLE_CELL","ART_GEOMETRY_LINE", "ART_CORNER", "ART_COLOUR_REGION"

## Filter Conditions Summary

| Condition Name | Descriptions |
| -------------- | ------------ |
| BarcodeFilteringCondition | Filter by the decoded barcodes information. |
| FrameFilteringCondition | Filter by the frames information. |
| TableCellFilteringCondition | Filter by the table cells information. |
| TextLineFilteringCondition | Filter by the recognized text lines information. |
| ColourRegionFilteringCondition | Filter by the colour regions information. |
| CornerFilteringCondition | Filter by the corners information. |
| GeometryLineFilteringCondition | Filter by the geometry lines information. |

## BarcodeFilteringCondition

Filter the reference objects by the decoded barcodes information. Barcode filtering is not implemented by default.

| Key Name | Value Range | Default Value |
| -------- | ----------- | ------------- |
| BarcodeFormatIds | One of the barcode format. | "BF_ALL" |
| BarcodeTextRegExPattern | N/A | "" |

### BarcodeFormatIds

Optional, 默认["BF_ALL"]

### BarcodeTextRegExPattern

".*b.*b.*b.*",
Optional，默认"", 不进行正则匹配

## FrameFilteringCondition

Filter the reference objects by the frame information. Barcode filtering is not implemented by default.

| Key Name | Value Range | Default Value |
| -------- | ----------- | ------------- |
| ImageDimensionRange |  |  |
| AspectRatioRange |  |  |
| WidthRange |  |  |
| HeightRange |  |  |

### ImageDimensionRange

: [16384,0x7fffffff], // Optional，默认[16384,0x7fffffff]

### AspectRatioRange

: [1, 10000], // Optional, 默认[1, 10000]. Aspect ratio equals to height/width*100.

### WidthRange

: [1, 0x7fffffff], // Optional, 默认[1, 0x7fffffff]

### HeightRange

: [1, 0x7fffffff], // Optional, 默认[1, 0x7fffffff]

## TableCellFilteringCondition

// For table cell filtering condition
// Optional, 默认null，表示不进行筛选
// 如果有多个Table, 则自动选择面积最大的Table

### RowNumbers

"1,3,5"

Optional,默认为""不进行筛选

### ColNumbers

"1"

Optional,默认为""不进行筛选

### RegionState

//Optional, 默认"default"，相当于全部；还可以是"selected"，表示只筛选选中的区域

## TextLineFilteringCondition

For label textline filtering condition

Optional, 默认null，表示不进行筛选

### LineNumbers

"1,3-5"
// Optional,默认为""不进行筛选

### LineStringRegExPattern

"Sodium[(\w| )]*"

Optional,默认为""不进行筛选

### RegionState

Optional, 默认"default"，相当于全部；还可以是"selected"，表示只筛选选中的区域

## ColourRegionFilteringCondition

// For colour region filtering condition
// Optional, 默认null，表示不进行筛选

### RegionPredetectionMode

"RPM_GENERAL"
Optional，默认为""不进行筛选

### ImageDimensionRange

[16384,0x7fffffff]
Optional，默认[16384,0x7fffffff]

### AspectRatioRange

Optional, 默认[1, 10000]. Aspect ratio equals to height/width*100.

### WidthRange

Optional, 默认[1, 0x7fffffff]

### HeightRange

Optional, 默认[1, 0x7fffffff]

## CornerFilteringCondition

For corner filtering condition
Optional, 默认null，表示不进行筛选
当前版本暂不考虑

### CornerPredetectionMode

"CPM_GENERAL"
Optional，默认为""不进行筛选

### CornerPredetectionModesIndex

Optional,默认为-1，不进行筛选

### AngleRange

[30,90]

Optional

## GeometryLineFilteringCondition

For line filtering condition
Optional, 默认null，表示不进行筛选
当前版本暂不考虑

### GeometryLinePredetectionMode

"LPM_GENERAL"
Optional，默认为""不进行筛选

### GeometryLinePredetectionModesIndex

Optional,默认为-1，不进行筛选

### AngleRange

[30,90]

Optional

### LengthRange

[10,100]

Optional
