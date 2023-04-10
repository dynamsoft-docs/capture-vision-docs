---
layout: default-layout
title: Location of TargetROIDefOption
description:
keywords:
needAutoGenerateSidebar: true
breadcrumbText:
---

# Location

Parameter `Location` defines where the `TargetROI` is. It consists the definition of `ReferenceObject` and the `Offset` attribute of the `TargetROI` base on the `ReferenceObject`. Of course, you can skip the definition of `ReferenceObject` to directly set the `Offset` attribute based on the original image.

```json
{
    //...
    "Location": 
    {
        "ReferenceObjectFilter" :
        {  
            "ReferenceTargetROIDefNameArray": ["TR_0"], 
            "AtomicResultTypeArray" : ["ART_BARCODE"], 
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

Defines the filter conditions of the `ReferenceObjects`. You can filter the reference objects by the `TargetROIDefName`, the type of the atomic results and even the further details of the atomic results. There might exist multiple objects that fit the filter conditions. As a result, the more appropriate the filter conditions are, the more accurate ROI locations you receive.

View more details about how to configure the [`ReferenceObjectFilter`](ReferenceObjectFilter.md) parameters.

### Offset

Defines the offset of the ROI from the reference object. The origin of the offset is the top-left vertex of the reference object. If there is no reference object defined, the origin will be set to the top-left vertex of the original image.

<div align="center">
   <p><img src="../../assets/location-offset.png" alt="Top level objects of DCV template file" width="50%" /></p>
   <p>Figure 1 – How to set Offset</p>
</div>

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

<div align="center">
   <p><img src="../../assets/define-location-with-reference-object.png" alt="set-reference-object" width="50%" /></p>
   <p>Figure 2 – How to define a <b>TargetROI</b> based on a <b>ReferenceObject</b></p>
</div>

```json
{
    //...
    "Location": 
    {
        "ReferenceObjectFilter" :
        {  
            "ReferenceTargetROIDefNameArray": ["TR_0"], // The ROI that you decoded the barcodes.
            "AtomicResultTypeArray" : ["ART_BARCODE"], // Set the AtomicResult type to barcode.
            // Set BarcodeFilteringCondition. Otherwise, all the barcodes will become ReferenceObject.
            "BarcodeFilteringCondition": 
            {
                "BarcodeFormatIds": ["BF_CODE_128"], // Use Code 128 only.
                "BarcodeTextRegExPattern": "/ReferenceObject/" // Find the Code 128 whose text has "ReferenceObject"
            }
        },
        "Offset" :
        {
            "ReferenceObjectOriginIndex": 0,
            "ReferenceObjectSizeType": "default",
            "MeasuredInPercentage" : 0, // Here we set it 0 to use the pixel.
            "FirstPoint" : [ 20, 140 ],
            "SecondPoint" : [ 210, 140 ],
            "ThirdPoint" : [ 210, 170 ],
            "FourthPoint" : [ 20, 170 ]
        }
    },
    //...
}
```
