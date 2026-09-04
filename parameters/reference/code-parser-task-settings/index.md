---
layout: default-layout
title: CodeParserTaskSetting Parameters - Dynamsoft Capture Vision
description: Reference index for CodeParserTaskSetting object in Dynamsoft Capture Vision parameters, which configure code parsing tasks such as passport MRZ, driving license, and other structured data.
keywords: CodeParserTaskSetting, code parser, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# CodeParserTaskSetting Parameters

The `CodeParserTaskSetting` object configures code parsing tasks such as passport MRZ, driving license, and other structured data parsing in Dynamsoft Capture Vision.

## Example JSON

```json
{
    "CodeParserTaskSettingOptions": [
        {
            "Name": "CPT1_PARSE_VIN",
            "CodeSpecifications": ["VIN"],
            "ResourcesPath": "../VIN/"
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `CodeParserTaskSetting` object inside `CodeParserTaskSettingOptions`.

```text
CodeParserTaskSetting
├── Name
├── CodeSpecifications
└── ResourcesPath
```

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the CodeParserTaskSetting object. |
| [`CodeSpecifications`](code-specifications.md) | The code specifications for parsing. |
| [`ResourcesPath`](resources-path.md) | The path to the resources directory for code parsing. |


