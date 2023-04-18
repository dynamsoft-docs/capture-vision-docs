---
layout: default-layout
title: Label Recognizer Task Setting - Dynamsoft Capture Vision Parameter File
description: Label Recognizer Task Setting object in the Dynamsoft Capture Vision Parameter File is an object for configuring and organizing the process of label recognition task.
keywords: label recognition, task, setting
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
---

# LabelRecognizerTaskSetting Object

The `LabelRecognizerTaskSetting` object is used to configure settings for a label recognition task to be performed on certain regions of interest (ROIs) in an image.

```json
{
    "Name" : "dlr_task_default",
    "TextLineSpecificationNameArray" : ["tls_default"],
    "DictionaryPath" : "",
    "DictionaryCorrectionThresholds" : [
        {
        "MaxWordLength" : 256,
        "MinWordLength" : 3,
        "Threshold" : 1
        }
    ],
    "StringLengthRange" : [3,200],
    "StringRegExPattern" : "",

    "SectionImageParameterArray":[
        {
            "Section": "REGION_PREDETECTION",
            "ImageParameterName": "ip_dlrDefault"
        },
        {
            "Section": "TEXT_LINE_LOCALIZATION",
            "ImageParameterName": "ip_dlrDefault"
        },
        {
            "Section": "TEXT_LINE_RECOGNITION",
            "ImageParameterName": "ip_dlrDefault"
        }
    ],
    "StartSection": "REGION_PREDETECTION",
    "TerminateSetting":
    {
        "Section": "REGION_PREDETECTION", 
        "Stage": "IRUT_GRAYSCALE_IMAGE",
    },
    "MaxThreadsInOneTask" : 4,
    "BaseLabelRecognizerTaskSettingName" : "",
}
```

<div align="center">
   <p>Example 1 – Parameters of LabelRecognizerTaskSetting</p>
</div>

## Summary of LabelRecognizerTaskSetting top-level parameters

| Parameter Name | Description |
| -------------- | ----------- |
| `Name` | Represents the name of the `LabelRecognizerTaskSetting` object, which serves as its unique identifier. |
| `TextLineSpecificationNameArray` | Represents the collection of text line specification object names, used to refer to the `TextLineSpecification` objects. It is used to define the recognition settings for the text lines. |
| `DictionaryPath` | Sets the path of the dictionary file. |
| `DictionaryCorrectionThresholds`| Sets the threshold of dictionary error correction.|
| `StringLengthRange` | Sets the range of string lengths for concatenated strings of recognized text lines.|
| `StringRegExPattern` | Specifies the regular expression pattern for concatenated strings of recognized text lines.|
| `SectionImageParameterArray` | Sets image parameters for three different sections, where each section performs image processing stages with different parameters.|
| `StartSection` | Indicates which Section the task will start executing from.|
| `TerminateSetting` | Indicates where the task stops, specifically indicating a Stage under a certain Section.|
| `MaxThreadsInOneTask` | Represents the maximum number of parallel threads that can be used on a single task.|
| `BaseLabelRecognizerTaskSettingName` | Represents the name of another `LabelRecognizerTaskSetting` object. It is used to inherit the parameters defined in its parent `LabelRecognizerTaskSetting` object. If a parameter has already been defined in this object, the parameter with the same name will not be inherited from the parent object.|