---
layout: default-layout
title: SemanticProcessing - Dynamsoft Capture Vision Parameter File
description: This page shows the SemanticProcessing object in the Dynamsoft Capture Vision Parameter File. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /parameters/file/semantic-processing/index.html
---

# SemanticProcessing Object

## Parameter Organization

A `SemanticProcessing` object is defined as below:

| Key Name | Value Type | Required or Optional | Description |
|---|---|---|---|
| Name | string | Mandatory | Sets the name of current `SemanticProcessing` object. The value must be unique between all `SemanticProcessing` objects. |
| ReferenceObjectFilter | JSON object | Optional | Sets a [ReferenceObjectFilter](#referenceobjectfilter) object to define the filter conditions |
| TaskSettingNameArray | string array | Optional | Sets the value for parameter [TaskSettingNameArray]({{site.parameters_reference}}task-setting-name-array.html) to define a group of semantic-processing tasks. |

Here is a sample:

```JSON
{
    "Name": "SP1_PARSE_VIN",
    "ReferenceObjectFilter": {
        "AtomicResultTypeArray": [
            "ART_BARCODE"
        ],
    }, 
    "TaskSettingNameArray": ["CPT1_PARSE_VIN"] 
}
```

### ReferenceObjectFilter

A `ReferenceObjectFilter` object is defined as below:

| Key Name | Value Type | Required or Optional | Description |
|---|---|---|---|
| ReferenceTargetROIDefNameArray | string array | Optional | A string array while each element is a string that represents the name of a `TargetROIDef` object. |
| AtomicResultTypeArray | string array | Optional | A string array while each element is a string that represents a type of atomic result that needs to be filtered |
| TextLineFilteringCondition | JSON object | Optional | An object used to specify the conditions for filtering text lines. |
| BarcodeFilteringCondition | JSON object | Optional | An object used to specify the conditions for filtering barcodes. |

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

## Design of Semantic Processing

The `SemanticProcessing` object is used to specify one or more tasks to analyze and extract information from image ROI processing results. The whole workflow typically involves following concepts.

## Prerequisites

A `SemanticProcessing` object will take effect when its name is referenced in `CaptureVisionTemplate.SemanticProcessingNameArray`.

## Launch Timing

The semantic process is triggered only after all the recognition tasks referenced in `CaptureVisionTemplate.ImageROIProcessingNameArray` have been completed.

## Data Filtering

In many cases, the process may involve filtering data to select only the relevant sources, such as a label text meeting a specific regular expression or a barcode meeting a specific format. `ReferenceObjectFilter` is used to specify such data filtering criteria.

## Task Execution

This is the main part of the workflow where the actual tasks are defined. `TaskSettingNameArray` is used to specify such tasks by referencing the name of a [`CodeParserTaskSetting`]({{site.parameter}}file/task-settings/code-parser-task-settings.html) object.

## Results Reporting

Currently, semantic-processing supports code parsing tasks, so the result is returned with callback [`OnParsedResultsReceived`]().
