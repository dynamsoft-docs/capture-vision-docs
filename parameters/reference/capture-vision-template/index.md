---
layout: default-layout
title: CaptureVisionTemplate Parameters - Dynamsoft Capture Vision
description: Reference index for CaptureVisionTemplate object in Dynamsoft Capture Vision parameters, the entry object of a parameter template that coordinates image sources, ROI processing, and semantic processing.
keywords: CaptureVisionTemplate, parameter reference
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# CaptureVisionTemplate Parameters

The `CaptureVisionTemplate` object is the entry object of a parameter template in Dynamsoft Capture Vision. It coordinates image sources, ROI processing, and semantic processing tasks.

## Example JSON

```json
{
    "CaptureVisionTemplates": [
        {
            "Name": "CV_0",
            "ImageSourceName": "ISA_0",
            "ImageROIProcessingNameArray": ["TA_0"],
            "SemanticProcessingNameArray": ["SP_0"],
            "OutputOriginalImage": 0,
            "MaxParallelTasks": 4,
            "MinImageCaptureInterval": 0,
            "Timeout": 500
        }
    ]
}
```

## Hierarchical Structure

This tree shows one `CaptureVisionTemplate` object inside `CaptureVisionTemplates`.

```text
CaptureVisionTemplate
├── Name
├── ImageSourceName
├── ImageROIProcessingNameArray
├── SemanticProcessingNameArray
├── OutputOriginalImage
├── MaxParallelTasks
├── MinImageCaptureInterval
└── Timeout
```

## Top-Level Parameters

| Parameter Name | Description |
|:---------------|:------------|
| [`Name`](name.md) | The unique name of the CaptureVisionTemplate object. |
| [`ImageSourceName`](image-source-name.md) | The name of the ImageSource object to use. |
| [`ImageROIProcessingNameArray`](image-roi-processing-name-array.md) | The names of TargetROIDef objects for ROI processing. |
| [`SemanticProcessingNameArray`](semantic-processing-name-array.md) | The names of SemanticProcessing objects for semantic processing. |
| [`OutputOriginalImage`](output-original-Image.md) | Whether to output the original image. |
| [`MaxParallelTasks`](max-parallel-tasks.md) | The maximum number of parallel tasks. |
| [`MinImageCaptureInterval`](min-image-capture-interval.md) | The minimum interval between image captures. |
| [`Timeout`](timeout.md) | The timeout for each capture. |


