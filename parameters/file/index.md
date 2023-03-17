---   
layout: default-layout
title: Structure of Dynamsoft Capture Vision Parameters
description: Introduce the parameter definitions, organization structure involved in Dynamsoft Capture Vision.
keywords: Parameter, Definition, Hierarchy
needAutoGenerateSidebar: true
noTitleIndex: true
---

# The Overall Structure of DCV Parameters

Dynamsoft Capture Vision (DCV) is an aggregating SDK of a series of specific functional products, which cover object capturing, content understanding, result parsing, and interactive viewing. To achieve high scalability and flexibility in DCV, a highly flexible and configurable parameter system has been designed to drive different behavior logic within the SDK.
This article provides an overview of the structure of parameters in Dynamsoft Capture Vision. In order to eliminate ambiguity, we first define a few conceptual nouns:

1. **Parameter**
A parameter is designed to represent a particular aspect of the behavior of the SDK, and each parameter has its own name. For instance, the 'ExpectedBarcodeCount' parameter is used to control the expected count of recognized barcodes. Parameters can be configured with specific values or ranges of values, which can be adjusted as required.

2. **Parameter template**
A parameter template is a collection of parameters organized in a structured manner, expressed in JSON format. The 'template name' is a unique identifier assigned to each parameter template. In the DCV SDK, this name is used to load the relevant configurations and control runtime behavior.
  
3. **Parameter template file**
A parameter template file is a JSON file that contains one or multiple parameter templates.

## Structure of the Parameter Template File

### Top-level Objects

<div align="center">
   <p><img src="./assets/parameter-template-file-example.png" alt="Top level objects of DCV template file" width="80%" /></p>
   <p>Figure 1 – Top level objects of DCV template file</p>
</div>

As shown in the figure above, the organizational structure of a parameter template file consists of several top-level objects, as shown below.

- `CaptureVisionTemplates`
- `ImageSourceOptions`
- `TargetROIDefOptions`
- `ImageParameterOptions`
- `BarcodeReaderTaskSettingOptions`
- `BarcodeFormatSpecificationOptions`
- `LabelRecognizerTaskSettingOptions`
- `TextLineSpecificationOptions`
- `DocumentNormalizerTaskSettingOptions`
- `SemanticProcessingOptions`
- `CodeParserTaskSettingOptions`
- `GlobalParameter`

With the exception of GlobalParameter, all top-level objects in the parameter template file are arrays of the corresponding object. For example,`CaptureVisionTemplates` are an array of `CaptureVisionTemplate` objects, and `TargetROIDefOptions` are an array of `TargetROIDef` objects. 
Furthermore, to reuse the same parameter definitions, reduce the size of the parameter template file, and simplify the parameter configuration hierarchy, a reference system based on the name was adopted in the parameter template file design. For example, the value of the `ImageSource` parameter for the first element in `CaptureVisionTemplates` is `ISA_0`, which refers to the first element in `ImageSourceOptions`.
Therefore, a parameter template starts with an element in `CaptureVisionTemplates` and recursively searches for the objects that are directly or indirectly referenced by it, and then combines them to form a specific set of parameters. Then, the parameter template may be applied to DCV to control its internal execution logic.
Next, we will focus on introducing some key objects in a parameter template and their reference relationships.

## Main Objects and Reference Relationships in Parameter Templates

The diagram below illustrates the main objects included in a complete parameter template, as well as the reference relationships between them. A solid green line indicates a one-to-one or one-to-zero correspondence, while a solid black line indicates a one-to-zero or one-to-n correspondence between the two objects.

<div align="center">
   <p><img src="./assets/dcv-template-reference-relationship.png" alt="Top level objects of DCV template file" width="100%" /></p>
   <p>Figure 2 – Object reference relationships in a parameter templates</p>
</div>

### CaptureVisionTemplate Object

This is the entry object of a parameter template in DCV. The `Name` parameter represents the name of the parameter template, which serves as its unique identifier. The key parameters under this object are as follows:

- **ImageSource**: Represents the input data source, which plays the role of the image source here.

- **ImageROIProcessingArray**: Represents the collection of image ROI processing definition objects. It is used to define recognition tasks performed on ROI of an image, including reading barcodes, recognizing labels, or detecting document quads.

- **SemanticProcessingArray**: Represents the collection of semantic processing objects.

For more details, please refer to this link.

### ImageSource Object

For more details, please refer to this link.

### TargetROIDef Object

For more details, please refer to this link.

### ImageParameter Object

For more details, please refer to this link.

### BarcodeReaderTaskSetting Object

For more details, please refer to this link.


### LabelRecognizerTaskSetting Object

For more details, please refer to this link.


### DocumentNormalizerTaskSetting Object

For more details, please refer to this link.


### SemanticProcessing Object

For more details, please refer to this link.

### CodeParserTaskSetting Object

For more details, please refer to this link.

## Special Rules of Parameter

### Inherited parameters

### Default Value of Parameters

