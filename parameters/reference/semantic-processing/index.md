---
layout: default-layout
title: SemanticProcessing Parameters - Dynamsoft Capture Vision
description: Reference index for SemanticProcessing object in Dynamsoft Capture Vision parameters, which defines semantic processing tasks and their input data filters.
keywords: SemanticProcessing, semantic processing, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# SemanticProcessing Parameters

The `SemanticProcessing` object specifies tasks to analyze and extract information from image ROI processing results.

## Example JSON

```json
{
    "SemanticProcessingOptions": [
        {
            "Name": "SP1_PARSE_VIN",
            "ReferenceObjectFilter": {
                "AtomicResultTypeArray": [
                    "ART_BARCODE"
                ]
            },
            "TaskSettingNameArray": ["CPT1_PARSE_VIN"]
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `SemanticProcessing` object inside `SemanticProcessingOptions`.

```text
SemanticProcessing
├── Name
├── ReferenceObjectFilter
└── TaskSettingNameArray
```

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique identifier for this `SemanticProcessing` object. |
| [`ReferenceObjectFilter`](reference-object-filter.md) | Defines filter conditions used to select source results for semantic processing. |
| [`TaskSettingNameArray`](task-setting-name-array.md) | The names of referenced `CodeParserTaskSetting` objects to execute. |
