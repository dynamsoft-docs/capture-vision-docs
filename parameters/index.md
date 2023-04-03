---
layout: default-layout
title: Parameters Introduction - Dynamsoft Capture Vision
description: This article introduces Dynamsoft Capture Vision Parameters.
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
permalink: /parameters/index.html
---

# Introduction to Dynamsoft Capture Vision Parameters

[Dynamsoft Capture Vision Architecture](../architecture/index.md) is designed to accommodate both entry-level needs and sophisticated business logic. While [Capture Vision Router](../architecture/index.md#capture-vision-router) allows developers to get started with image processing in their applications within hours, the Dynamsoft Capture Vision (DCV) parameters are what make it possible for the applications to be able to handle all sorts of image processing scenarios without changing the code much.

Simply put, DCV parameters are used to configure how different functional products work in the Dynamsoft Capture Vision architecture.

These docs help you learn and use the DCV parameters.

## Parameter File

The following topics are covered in the [Parameter File Overview](file/index.md):

- [Organization of a Parameter Template File](file/index.md#organization-of-a-parameter-template-file). A template file contains one or multiple templates.
- [Structure of a Parameter Template](file/index.md#structure-of-a-parameter-template). A template is a predefined configuration of parameters.
- [How to Apply DCV Parameters](file/index.md#how-to-apply-dcv-parameters). This topic discusses how to interact with DCV to import or update templates.
- [Special Rules for DCV Parameter Configuration](file/index.md#special-rules-for-dcv-parameter-configuration). This topic talks about special rules to note when defining templates.

Then each of the objects that make up a Parameter File is introduced in detail:

- [CaptureVisionTemplate](file/capture-vision-template.md). `CaptureVisionTemplates` in a parameter file contains one or multiple `CaptureVisionTemplate`.
- [ImageSource]

    "": [ 
        {
            "Name": "ISA_0"
        }
    ],
    "Options" : [
        {
            "Name" : "TA_0",
            "TaskSettingNameArray": [ "LR_0", "BR_0", "DN_0" ]
        }
    ],
    "ImageParameterOptions": [
        {
            "Name": "IP_0"
        }
    ], 
    "BarcodeReaderTaskSettingOptions": [
        {
            "Name" : "BR_0",
            "BarcodeFormatSpecificationNameArray" : ["FS_0"]
        }
    ],
    "BarcodeFormatSpecificationOptions": [
        {
            "Name": "FS_0"
        }
    ],
    "LabelRecognizerTaskSettingOptions": [
        {
            "Name" : "LR_0",
            "TextLineSpecificationNameArray" : [ "LS_0" ]
        }
    ],
    "TextLineSpecificationOptions" : [
        {
            "Name" : "LS_0",
            "CharacterModelName" : "NumberLetter"
        }
    ],
    "CharacterModelOptions" : [
        {
            "Name" : "NumberLetter"
        }
    ],
    "DocumentNormalizerTaskSettingOptions": [
        {
            "Name" : "DN_0"
        }
    ],
    "SemanticProcessingOptions": [
        {
            "Name": "SP_0",
            "TaskSettingNameArray": [
                "CP_0"
            ]
        }
    ],
    "CodeParserTaskSettingOptions": [
        {
            "Name": "CP_0"
        }
    ],
    "GlobalParameter":{
        "MaxTotalImageDimension":0
    }
}