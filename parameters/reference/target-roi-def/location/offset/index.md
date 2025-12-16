---
layout: default-layout
title:  Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needGenerateH3Content: true
---
# Offset

Parameter `Offset` is an object that defines how the location is offset from the `reference object` or the original image. It includes the following child parameters:

```json
{
    "Offset": {
        "ReferenceObjectOriginIndex": 0,
        "ReferenceObjectType": "ROT_ATOMIC_OBJECT",
        "ReferenceXAxis": {},
        "ReferenceYAxis": {},
        "MeasuredByPercentage" : 1,
        "FirstPoint" : [ 0, 0 ],
        "SecondPoint" : [ 100, 0 ],
        "ThirdPoint" : [ 100, 100 ],
        "FourthPoint" : [ 0, 100 ]
    }
}
```

| Name | Description |
| ---- | ----------- |
| [`ReferenceObjectOriginIndex`](offset-parameter-details.md#referenceobjectoriginindex) | Defines which point of the reference object will be set as the origin of the coordinate system. |
| [`ReferenceObjectType`](offset-parameter-details.md#referenceobjecttype) | Defines which coordinate system to use when configuring offset parameters basd on the reference objects. |
| [`ReferenceXAxis`](reference-x-axis.md) | Defines the x-axis of the coordinate system to use when configuring offset parameters basd on the reference objects. |
| [`ReferenceYAxis`](reference-y-axis.md) | Defines the y-axis of the coordinate system to use when configuring offset parameters basd on the reference objects. |
| [`MeasuredByPercentage`](offset-parameter-details.md#measuredbypercentage) | Sets whether or not to use percentage to measure the points' coordinates. |
| [`FirstPoint`](offset-parameter-details.md#firstpoint) | Specifies the top-left vertex of the ROI. |
| [`SecondPoint`](offset-parameter-details.md#secondpoint) | Specifies the top-right vertex of the ROI. |
| [`ThirdPoint`](offset-parameter-details.md#thirdpoint) | Specifies the bottom-right vertex of the ROI. |
| [`FourthPoint`](offset-parameter-details.md#fourthpoint) | Specifies the bottom-left vertex of the ROI. |
