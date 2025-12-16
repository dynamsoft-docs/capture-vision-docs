---   
layout: default-layout
title: Overview of Dynamsoft Capture Vision Parameters
description: Introduce the overview parameters design of Dynamsoft Capture Vision.
keywords: Parameter, Parameter Template, Parameter Template File
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# Overview of DCV parameters

Dynamsoft Capture Vision (DCV) is designed for high scalability and flexibility, and its parameter system plays a crucial role in achieving that. The parameter system can drive the behaviour of the SDK through its many varied configurations. In this article, we will provide an overview of the parametric architecture design of Dynamsoft Capture Vision.

## Key Terms

In order to eliminate ambiguity, we first define several key terms.

- **Parameter** - A parameter is designed to represent a particular aspect of the behavior of the SDK, and each parameter has its own name. For instance, the `ExpectedBarcodesCount` parameter is used to control the expected number of recognized barcodes in the image or frame. Parameters can be configured with specific values or a range of values, which can be adjusted as required.

- **Parameter template** - A parameter template is a collection of parameters organized in a structured manner, expressed in JSON format. The name of the `CaptureVisionTemplate` object is also called "template name", which is a unique identifier assigned to each parameter template. In the DCV SDK, this name is used to load the relevant configurations and control runtime behavior.
  
- **Parameter template file** - A parameter template file is a JSON file that contains one or multiple parameter templates.

## Organization of a Parameter Template File

With the exception of `GlobalParameter`, all top-level keys in the parameter template file are arrays of the corresponding object. For example,`CaptureVisionTemplates` is an array of `CaptureVisionTemplate` objects, and `TargetROIDefOptions` is an array of `TargetROIDef` objects, and so on.

> [!NOTE]
> **For Dynamsoft Barcode Reader SDK Users:**
> 
> When using Dynamsoft Barcode Reader SDK standalone (without other DCV functional products), the following objects and their parameters are not applicable:
> - `LabelRecognizerTaskSettingOptions`
> - `DocumentNormalizerTaskSettingOptions`
> - `CodeParserTaskSettingOptions`
> - `OutputTaskSettingOptions`
> - `TextLineSpecificationOptions`
> - `SemanticProcessingOptions`

The following table list all the top-level keys.

| Key Name                   | Description  |
| :--------------------------| :----------- |
| `CaptureVisionTemplates` | Array of [CaptureVisionTemplate]({{site.dcvb_parameters}}file/capture-vision-template.html) objects. `CaptureVisionTemplate` is the entry object of a parameter template in DCV. The `Name` parameter represents the name of the parameter template, which serves as its unique identifier.|
| `ImageSourceOptions` | Array of [ImageSource]({{site.dcvb_parameters}}file/image-source.html) objects. `ImageSource` defines the input for DCV responsible for providing images to DCV. It can be defined as different image sources, including but not limited to, image directories, scanners, cameras, etc.|
| `TargetROIDefOptions` | Array of [TargetROIDef]({{site.dcvb_parameters}}file/target-roi-definition/index.html) objects. `TargetROIDef` specifies one or more recognition tasks to be performed on some regions of interest (ROIs) within an image.|
| `BarcodeReaderTaskSettingOptions` | Array of [BarcodeReaderTaskSetting]({{site.dcvb_parameters}}file/task-settings/barcode-reader-task-settings.html) objects. `BarcodeReaderTaskSetting` configures the settings for barcode reading tasks performed on images in DCV. |
| `LabelRecognizerTaskSettingOptions` | Array of [LabelRecognizerTaskSetting]({{site.dcvb_parameters}}file/task-settings/label-recognizer-task-settings.html) objects. `LabelRecognizerTaskSetting` configures the settings for label recognition tasks performed on images in DCV.|
| `DocumentNormalizerTaskSettingOptions` | Array of [DocumentNormalizerTaskSetting]({{site.dcvb_parameters}}file/task-settings/document-normalizer-task-settings.html) objects. `DocumentNormalizerTaskSetting` configures the settings for the document detection or normalization process of an image in DCV. |
| `CodeParserTaskSettingOptions` | Array of [CodeParserTaskSetting]({{site.dcvb_parameters}}file/task-settings/code-parser-task-settings.html) objects. `CodeParserTaskSetting` configures the code parsing tasks such as passport MRZ, driving license and other user specific tasks in DCV etc.|
| `OutputTaskSettingOptions` | Array of [OutputTaskSetting]({{site.dcvb_parameters}}file/task-settings/output-task-setting.html) objects. `OutputTaskSetting` configures how to output the expected results of the ancestor `TargetROIDef` by filtering the results of the descendant `TargetROIDef` object. |
| `ImageParameterOptions` | Array of [ImageParameter]({{site.dcvb_parameters}}file/image-parameter.html) objects. `ImageParameter` provides various image-processing features to adjust and enhance the input image for better recognition results.|
| `BarcodeFormatSpecificationOptions` | Array of [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/capture-vision-model.html) objects. `BarcodeFormatSpecification` sets configurations for specified barcode formats.|
| `TextLineSpecificationOptions` | Array of [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/textline-specification.html) objects. `TextLineSpecification` defines configurations for the specified text lines.|
| `CaptureVisionModelOptions` | Array of [CaptureVisionModel]({{ site.dcvb_parameters }}file/auxiliary/capture-vision-model.html) objects. `CaptureVisionModel` defines how the library find Convolutional Neural Networks (CNN) model files.|
| [GlobalParameter]({{ site.dcvb_parameters }}file/auxiliary/global-parameter.html) | Defines the global parameters.|
| `SemanticProcessingOptions` | Array of [SemanticProcessing]({{site.dcvb_parameters}}file/semantic-processing/index.html) objects. `SemanticProcessing` specifies one or more code parsing tasks to be performed on text/byte results to help extract human readable information. |


### Full JSON Structure

The following example shows the full JSON structure used by Dynamsoft Capture Vision.

```json
{
    "CaptureVisionTemplates": [
        {
            "Name" : "CV_0",
            "ImageSourceName": "ISA_0",
            "ImageROIProcessingNameArray": ["TA_0" ],
            "SemanticProcessingNameArray": ["SP_0"]
            // ...other optional parameters
        },
        {
            // another CaptureVisionTemplate object
        }
    ],
    "ImageSourceOptions": [ 
        {
            "Name": "ISA_0"
            // ...other optional parameters
        },
        {
            // another ImageSource object
        }
    ],
    "TargetROIDefOptions" : [
        {
            "Name" : "TA_0",
            "TaskSettingNameArray": [ "LR_0", "BR_0", "DN_0" ]
            // ...other optional parameters
        },
        {
            // another TargetROIDef object
        }
    ],
    "ImageParameterOptions": [
        {
            "Name": "IP_0"
            // ...other optional parameters
        },
        {
            // another ImageParameter object
        }
    ], 
    "BarcodeReaderTaskSettingOptions": [
        {
            "Name" : "BR_0",
            "BarcodeFormatSpecificationNameArray" : ["FS_0"]
            // ...other optional parameters
        },
        {
            // another BarcodeReaderTaskSetting object
        }
    ],
    "BarcodeFormatSpecificationOptions": [
        {
            "Name": "FS_0"
            // ...other optional parameters
        },
        {
            // another BarcodeFormatSpecification object
        }
    ],
    "LabelRecognizerTaskSettingOptions": [
        {
            "Name" : "LR_0",
            "TextLineSpecificationNameArray" : [ "LS_0" ]
            // ...other optional parameters
        },
        {
            // another LabelRecognizerTaskSetting object
        }
    ],
    "TextLineSpecificationOptions" : [
        {
            "Name" : "LS_0",
            "CharacterModelName" : "NumberLetterCharRecognition"
            // ...other optional parameters
        },
        {
            // another TextLineSpecification object
        }
    ],
    "CaptureVisionModelOptions" : [
        {
            "Name" : "NumberLetterCharRecognition"
            // ...other optional parameters
        },
        {
            // another CaptureVisionModel object
        }
    ],
    "DocumentNormalizerTaskSettingOptions": [
        {
            "Name" : "DN_0"
            // ...other optional parameters
        },
        {
            // another DocumentNormalizerTaskSetting object
        }
    ],
    "SemanticProcessingOptions": [
        {
            "Name": "SP_0",
            "TaskSettingNameArray": [
                "CP_0"
            ]
            // ...other optional parameters
        },
        {
            // another SemanticProcessing object
        }
    ],
    "CodeParserTaskSettingOptions": [
        {
            "Name": "CP_0"
            // ...other optional parameters
        },
        {
            // another CodeParserTaskSetting object
        }
    ],
    "GlobalParameter":{
        "MaxTotalImageDimension": 0
        // ...other optional parameters
    },
    "OutputTaskSettingOptions":[
        {
            "Name" : "output_task"
            // ...other optional parameters
        },
        {
            // another OutputTaskSetting object
        }
    ]
}
```

> [!IMPORTANT]
> This example shows the complete JSON structure template.
> Most fields are optional and should be included only when needed.
> Do NOT copy this whole structure directly.
> For real usage, start with the Minimal Valid JSON example and add only the necessary sections.


### Minimal Valid JSON Example

The following example includes only the minimum required fields needed to create a functional configuration.
You can use it as a starting point and expand it based on your scenario.

```json
{
    "CaptureVisionTemplates": [
        {
            "Name" : "CV_0",
            "ImageROIProcessingNameArray": ["TA_0" ],
        }
    ],
    "TargetROIDefOptions" : [
        {
            "Name" : "TA_0",
            "TaskSettingNameArray": [ "BR_0" ]
        }
    ],
    "BarcodeReaderTaskSettingOptions": [
        {
            "Name" : "BR_0",
            "BarcodeFormatIds": ["BF_DEFAULT"]
        }
    ]
}
```

> [!NOTE]
> This minimal example is intentionally simple.
> In real-world scenarios, additional sections such as `ImageParameter`, `LabelRecognizerTaskSetting`, or `SemanticProcessing` options may be required depending on the features you use.

## How to Apply DCV Parameters

To use custom parameters in Dynamsoft Capture Vision, follow these steps:

1. **Load Parameter Template**
   
   Use one of the following APIs to load your parameter template:
   - `InitSettings(jsonString)` - Load parameter template from a JSON string
   - `InitSettingsFromFile(filePath)` - Load parameter template from a JSON file
   
   > [!NOTE]
   > These APIs will replace all existing parameter templates with the ones from the loaded content.

2. **Start Capturing**
   
   Pass the template name to one of the capturing APIs:
   - `Capture(..., templateName)` - Processes a single-page image.
   - `CaptureMultiPages(..., templateName)` - Processes a multiple-page image.
   - `StartCapturing(..., templateName)` - Starts continuous capturing to process multiple images.
   
   The `templateName` parameter should match the `Name` field in your `CaptureVisionTemplate` object.

3. **Reset to Default (Optional)**
   
   If you need to discard custom settings and restore factory defaults:
   - `ResetSettings()` - Resets all parameter templates to their original factory state
   
   This is useful when you want to start fresh or switch between different configuration modes.

## Special Rules for DCV Parameter Configuration

In this section, we will discuss some special rules for configuring the DCV parameter templates. Understanding these rules will help you efficiently configure a simple and user-friendly parameter template.

### Default Value of Parameters

Generally, the DCV parameter templates have been designed with many common scenarios in mind, so the default values of many parameters do not need to be modified. When configuring a custom template, you only need to configure required parameters and fine-tuning parameters related to business scenarios. Other optional parameters are automatically filled with default values. This simplifies your configuration and makes your templates easier to read.

### Inherited Parameters

Sometimes, we need to configure multiple templates to adapt to different scenarios, but only a few parameter values differ between each template. DCV provides a parameter configuration inheritance mechanism that further reduces the amount of configuration work.
For example, when configuring `IP_A` and `IP_B` objects in `ImageParameterOptions`, you can define a `BaseImageParameterName` parameter in the `IP_B` object with a value of `IP_A`. Then `IP_B` object will inherit all the parameter definitions of `IP_A`, and if `IP_B` defines a parameter with the same name but a different value, that parameter will adopt the value of `IP_B`.

This allows you to create a new parameter template that inherits most of its configuration from an existing template, reducing the amount of repetitive configuration work needed.
