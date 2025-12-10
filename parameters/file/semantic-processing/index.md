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
| [Name]({{site.dcvb_parameters_reference}}semantic-processing/name.html) | string | Mandatory | Sets the name of current `SemanticProcessing` object. The value must be unique between all `SemanticProcessing` objects. |
| [ReferenceObjectFilter]({{site.dcvb_parameters_reference}}semantic-processing/reference-object-filter.html) | JSON object | Optional | Sets a [ReferenceObjectFilter](#referenceobjectfilter) object to define the filter conditions. |
| [TaskSettingNameArray]({{site.dcvb_parameters_reference}}semantic-processing/task-setting-name-array.html) | string array | Optional | Represents the collection of task setting object names, used to refer to the `CodeParserTaskSetting` objects. |

Here is a sample:

```json
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

## Design of Semantic Processing

The `SemanticProcessing` object is used to specify one or more tasks to analyze and extract information from image ROI processing results. The whole workflow typically involves following concepts.

### Prerequisites

A `SemanticProcessing` object will take effect when its name is referenced in `CaptureVisionTemplate.SemanticProcessingNameArray`.

### Launch Timing

The semantic process is triggered only after all the recognition tasks referenced in `CaptureVisionTemplate.ImageROIProcessingNameArray` have been completed.

### Data Filtering

In many cases, the process may involve filtering data to select only the relevant sources, such as a label text meeting a specific regular expression or a barcode meeting a specific format. `ReferenceObjectFilter` is used to specify such data filtering criteria.

### Task Execution

This is the main part of the workflow where the actual tasks are defined. `TaskSettingNameArray` is used to specify such tasks by referencing the name of a [`CodeParserTaskSetting`]({{site.dcvb_parameters}}file/task-settings/code-parser-task-settings.html) object.

### Results Reporting

Currently, semantic-processing supports code parsing tasks, so the result is returned with callback `OnParsedResultsReceived`.
