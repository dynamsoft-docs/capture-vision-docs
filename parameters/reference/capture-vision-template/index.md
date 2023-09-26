---
layout: default-layout
title: Index - CaptureVisionTemplate Parameters
description: The index of CaptureVisionTemplate parameters.
keywords: CaptureVisionTemplate, parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/capture-vision-template/index.html
---

# CaptureVisionTemplate Parameters

```json
{
    "Name" : "CV_0",
    "ImageSourceName": "ISA_0",
    "ImageROIProcessingNameArray": ["TA_0" ],
    "SemanticProcessingNameArray": ["SP_0"],
    "OutputOriginalImage": 0,
    "MaxParallelTasks" : 4,
    "Timeout" : 500
}
```

| Parameter Name | Description |
| -------------- | ----------- |
| [`ImageROIProcessingNameArray`](image-roi-processing-name-array.md) | Defines the collection of image ROI processing object names, used to refer to the `TargetROIDef` objects. |
| [`ImageSourceName`](image-source-name.md) | Indicates the input source name, used to refer to the `ImageSource` object. |
| [`MaxParallelTasks`](max-parallel-tasks.md) | Defines the maximum number of parallel tasks for the DCV runtime. |
| [`Name`](name.md) | Defines the name of a `CaptureVisionTemplate` object, which serves as its unique identifier. |
| [`OutputOriginalImage`](output-original-Image.md) | Indicates whether DCV finally outputs the original input image. |
| [`SemanticProcessingNameArray`](semantic-processing-name-array.md) | Represents the collection of semantic-processing object names, used to refer to the `SematicProcessing` objects. |
| [`Timeout`](timeout.md) | Defines the maximum amount of time (in milliseconds) that should be spent processing each image or frame. |
