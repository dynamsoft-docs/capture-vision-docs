---
layout: default-layout
title:  Dynamsoft Capture Vision Parameters
description: The parameter Location of Dynamsoft Capture Vision defines the location information of the ROIs.
keywords: Location
needGenerateH3Content: true
---
# ReferenceObjectFilter

Parameter `ReferenceObjectFilter` is a group of filter conditions for figuring out the `reference objects`.

```json
{
    "ReferenceObjectFilter":
    {
        "ReferenceTargetROIDefNameArray": [], 
        "AtomicResultTypeArray" : ["ART_TEXT_LINE","ART_BARCODE","ART_FRAME"], 
        "ReferenceTaskNameArray": ["DBR_task"], 
        "BarcodeFilteringCondition": {},
        "FrameFilteringCondition": {},
        "TextLineFilteringCondition":{},
        "RegionFilteringCondition": {
            "RegionPredetectionMode": "RPM_GENERAL",
            "LabelIdArray": [0, 1, 2]
        }
    }
}
```

| Name | Description |
| ---- | ----------- |
| [`ReferenceTargetROIDefNameArray`](reference-object-filter-parameter-details.md#referencetargetroidefnamearray) | Filter the reference object by specifying `TargetROI` names. |
| [`AtomicResultTypeArray`](reference-object-filter-parameter-details.md#atomicresulttypearray) | Filter the reference object by specifying the type of atomic results. |
| [`ReferenceTaskNameArray`](reference-object-filter-parameter-details.md#referencetasknamearray) | Filter the reference object by specifying the reference task name array. |
| [`BarcodeFilteringCondition`](barcode-filtering-condition.md) | One of the filter conditions. Filter the reference objects with the decoded barcode information. |
| [`FrameFilteringCondition`](frame-filtering-condition.md) | One of the filter conditions. Filter the reference objects with the frame information. |
| [`RegionFilteringCondition`](region-filtering-condition.md) | One of the filter conditions. Filter the reference objects with the predetected region information. |
| [`TextLineFilteringCondition`](text-line-filtering-condition.md) | One of the filter conditions. Filter the reference objects with the text line content. |
