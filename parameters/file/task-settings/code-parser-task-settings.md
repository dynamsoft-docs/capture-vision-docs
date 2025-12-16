---
layout: default-layout
title: CodeParserTaskSetting - Dynamsoft Capture Vision Parameter File
description: The CodeParserTaskSetting object in the Dynamsoft Capture Vision Parameter File. 
needAutoGenerateSidebar: false
---

# CodeParserTaskSetting Object

The `CodeParserTaskSetting` object defines configurations for parsing barcode text into structured data fields. It specifies which code specification files to use and where to find the parsing resources.

## Example

```json
{
    "Name": "CPT1_PARSE_VIN",
    "CodeSpecifications": ["VIN"],
    "ResourcesPath": "../VIN/" 
}
```

## Parameters

A `CodeParserTaskSetting` object contains the following parameters:

| Parameter Name | Type | Required/Optional | Description |
|---|---|---|---|
| [`Name`]({{site.dcvb_parameters_reference}}code-parser-task-settings/name.html) | String | Required | The unique identifier for this `CodeParserTaskSetting` object. Must be unique among all task setting objects. |
| [`CodeSpecifications`]({{site.dcvb_parameters_reference}}code-parser-task-settings/code-specifications.html) | String Array | Optional | An array of code specification file names that define how to parse the barcode text into structured fields. |
| [`ResourcesPath`]({{site.dcvb_parameters_reference}}code-parser-task-settings/resources-path.html) | String | Optional | The directory path containing the resources needed for code parsing (e.g., specification files, models). |
