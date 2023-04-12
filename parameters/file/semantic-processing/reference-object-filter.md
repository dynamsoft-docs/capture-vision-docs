---
layout: default-layout
title: ReferenceObjectFilter - Dynamsoft Capture Vision Parameter File
description: This page shows the ReferenceObjectFilter object in the Dynamsoft Capture Vision Parameter File. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /parameters/file/semantic-processing/reference-object-filter.html
---

# ReferenceObjectFilter

## Parameter Organization

A `ReferenceObjectFilter` object is defined as below:

| Key Name | Value Type | Required or Optional | Description |
|---|---|---|---|
| ReferenceTargetROIDefNameArray | string array | Optional | A string array while each element is a string that represents the name of a `TargetROIDef` object. |
| AtomicResultTypeArray | string array | Optional | A string array while each element is a string that represents a type of atomic result that needs to be filtered |
| TextLineFilteringCondition | string array | Optional | An object used to specify the conditions for filtering text lines. |
| BarcodeFilteringCondition | string array | Optional | An object used to specify the conditions for filtering barcodes. |

Here is a sample:

```JSON
{
    "ReferenceObjectFilter" :
    {  
        "ReferenceTargetROIDefNameArray": ["TR_0", "TR_1"], 
        "AtomicResultTypeArray" : ["ART_TEXT_LINE","ART_BARCODE"], 
        "BarcodeFilteringCondition": 
        {
            "BarcodeFormatIds": ["BF_CODE39"], 
            "BarcodeTextRegExPattern": ".*b.*b.*b.*"
        },
        "TextLineFilteringCondition":
        {
            "LineNumbers": "1,3-5",  
            "LineStringRegExPattern": "P<CAN[A-Z<]{39}"
        }
    }
}
```
