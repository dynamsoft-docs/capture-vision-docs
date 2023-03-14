---
layout: default-layout
title: Location of TargetROIDefOption
description:
keywords:
needAutoGenerateSidebar: true
breadcrumbText:
---

# Location

`Location` Determines how the location(s) of ROI(s) are defined. You can either define the vertices coordinates of the ROI on the original image or define how to localize the ROI(s) by referencing a previously captured atomic result.

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
            "GeometryLineFilteringCondition": {}
        },
        "Offset" :
        {
            "ReferenceObjectOriginIndex": 0,
            "ReferenceObjectSizeType": "default",
            "MeasuredInPercentage" : 1,
            "FirstPoint" : [ 0, 0 ],
            "SecondPoint" : [ 100, 0 ],
            "ThirdPoint" : [ 100, 100 ],
            "FourthPoint" : [ 0, 100 ]
        }
    },
    //...
}
```

## Parameter Summary

### ReferenceObjectFilter

Defines the filter conditions of the reference objects. You can filter the reference objects by the `TargetROIDefName`, the type of the atomic results and even the further details of the atomic results. There might exist multiple objects that fit the filter conditions. As a result, the more appropriate the filter conditions are, the more accurate ROI locations you receive.

### Offset

Defines the offset of the ROI from the reference object. The origin of the offset is the top-left vertex of the reference object. If there is no reference object defined, the origin will be set to the top-left vertex of the original image.

## How to Use

### Define a Target ROI Based on the Original Image

Even if you don't hava any reference object, you can still set a offset based on the original image to localize the ROI. The following code snippet shows how to defines a ROI on the top-right corner of the image.

```json
{
    //...
    "Location": 
    {
        "Offset" :
        {
            "ReferenceObjectOriginIndex": 0,
            "ReferenceObjectSizeType": "default",
            "MeasuredInPercentage" : 1,
            "FirstPoint" : [ 0, 0 ],
            "SecondPoint" : [ 100, 0 ],
            "ThirdPoint" : [ 100, 100 ],
            "FourthPoint" : [ 0, 100 ]
        }
    },
    //...
}
```

### Define a Target ROI Based on a Reference Object

If the there exists significant objects that can help you localizing the targeting content. You can define filter conditions to localize the reference object first and then capture the targeting content.

The following example shows how to define the `ReferenceObjectFilter` to use the barcode location information to extract the certain text line information:

![Example - Define a Target ROI Based on a Reference Object](example-reference-obj-filter.jpg)

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
            "GeometryLineFilteringCondition": {}
        },
        "Offset" :
        {
            "ReferenceObjectOriginIndex": 0,
            "ReferenceObjectSizeType": "default",
            "MeasuredInPercentage" : 1,
            "FirstPoint" : [ 0, 0 ],
            "SecondPoint" : [ 100, 0 ],
            "ThirdPoint" : [ 100, 100 ],
            "FourthPoint" : [ 0, 100 ]
        }
    },
    //...
}
```
