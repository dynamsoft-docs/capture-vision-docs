---
layout: default-layout
title: SemanticProcessing - Dynamsoft Capture Vision Parameter File
description: This page shows the SemanticProcessing object in the Dynamsoft Capture Vision Parameter File. 
---

# SemanticProcessing Object

The `SemanticProcessing` object specifies tasks to analyze and extract information from image ROI processing results.

## Example

```json
{
    "Name": "SP1_PARSE_VIN",
    "ReferenceObjectFilter": {
        "AtomicResultTypeArray": [
            "ART_BARCODE"
        ]
    },
    "TaskSettingNameArray": ["CPT1_PARSE_VIN"]
}
```

## Parameters

| Parameter Name | Type | Required/Optional | Description |
| -------------- | ---- | ----------------- | ----------- |
| [`Name`]({{site.dcvb_parameters_reference}}semantic-processing/name.html) | String | Required | The unique identifier for this SemanticProcessing object. |
| [`ReferenceObjectFilter`]({{site.dcvb_parameters_reference}}semantic-processing/reference-object-filter.html) | Object | Optional | Defines filter conditions to select relevant data sources for processing. |
| [`TaskSettingNameArray`]({{site.dcvb_parameters_reference}}semantic-processing/task-setting-name-array.html) | String Array | Optional | Array of CodeParserTaskSetting object names defining the parsing tasks to execute. |

## Workflow

The semantic processing workflow involves the following stages:

### Prerequisites

A `SemanticProcessing` object takes effect when its name is referenced in `CaptureVisionTemplate.SemanticProcessingNameArray`.

### Launch Timing

The semantic process triggers only after all recognition tasks referenced in `CaptureVisionTemplate.ImageROIProcessingNameArray` have been completed.

### Data Filtering

The process may involve filtering data to select relevant sources, such as label text matching a specific regular expression or barcodes meeting a specific format. Use `ReferenceObjectFilter` to specify data filtering criteria.

### Task Execution

This is where actual tasks are defined. Use `TaskSettingNameArray` to specify tasks by referencing [`CodeParserTaskSetting`]({{site.dcvb_parameters}}file/task-settings/code-parser-task-settings.html) object names.

### Results Reporting

Currently, semantic-processing supports code parsing tasks. Results are returned with the `OnParsedResultsReceived` callback.
