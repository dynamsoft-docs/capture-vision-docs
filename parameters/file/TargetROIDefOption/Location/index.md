---
layout: default-layout
title: Location of TargetROIDefOption
description:
keywords:
needAutoGenerateSidebar: true
breadcrumbText:
---

# Location

`Location` determines how the location of a target ROI is defined. You can either define the vertices coordinates of the ROI on the original image or define how to localize the target ROI by referencing a previously captured atomic result.

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

View more details about how to configure the [`ReferenceObjectFilter`](ReferenceObjectFilter.md)

### Offset

Defines the offset of the ROI from the reference object. The origin of the offset is the top-left vertex of the reference object. If there is no reference object defined, the origin will be set to the top-left vertex of the original image.

View more details about how to configure the [`Offset`](Offset.md)

## How to Use

### Define a Target ROI Based on the Original Image

Even if you don't hava any reference object, you can still set a offset based on the original image to localize the ROI. The following code snippet shows how to defines a ROI on the top-right corner of the image.

For example, you are going to decode barcode from the original image.

* Step 1: Define a `TargetROI`
  * Step 1.1: Name your `TargetROI` "ROI_0".
  * Step 1.2: Define the location of the "ROI_0" leave the `ReferenceObjectFilter` empty.
  * Step 1.3: Define the Offset.
* Step 2: Define a barcode decoding task in `BarcodeReaderTaskSettingOptions`. Name the task "BR_0".
* Step 3: Add "ROI_0" to the `ImageROIProcessingNameArray` so that the results captured from the "ROI_0" are output.

```json
{
    "CaptureVisionTemplates": 
    [
        {
            "Name" : "CV_0",
            "ImageSourceName": "CameraEnhancer_0",
            "ImageROIProcessingNameArray": ["ROI_0"]     
        }
    ],
    "TargetROIDefOptions": 
    [
        {
            "Name": "ROI_0",
            "TaskSettingNameArray": ["BR_0"],
            "Location": 
            {
                "Offset":
                {
                    "ReferenceObjectOriginIndex": 0,
                    "ReferenceObjectSizeType": "default",
                    "MeasuredInPercentage": 1,
                    "FirstPoint": [ 0, 0 ],
                    "SecondPoint": [ 100, 0 ],
                    "ThirdPoint": [ 100, 100 ],
                    "FourthPoint": [ 0, 100 ]
                }
            },
        }
    ],
    "BarcodeReaderTaskSettingOptions":
    [
        {
            // Your barcode decoding settings
        }
    ]
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
