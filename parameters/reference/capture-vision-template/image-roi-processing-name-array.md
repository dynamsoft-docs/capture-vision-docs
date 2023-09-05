---
layout: default-layout
title: ImageROIProcessingNameArray - Dynamsoft Capture Vision Parameters
description: The parameter ImageROIProcessingNameArray of Dynamsoft Capture Vision defines the collection of image ROI processing object names.
keywords: image ROI processing, TargetROIDef, CaptureVisionTemplate
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/capture-vision-template/image-roi-processing-name-array.html
---

# ImageROIProcessingNameArray

Parameter `ImageROIProcessingNameArray` defines the collection of image ROI processing object names, used to refer to the `TargetROIDef` objects

## Example

```json
{
    "ImageROIProcessingNameArray": ["dlr_roi"]
}
```

## Parameter Summary

| ImageROIProcessingNameArray Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element is the name of a `TargetROIDef` object. |
| **Default Value**<br>['roi_default'] |
| **Remarks**<br>If `ImageROIProcessingNameArray` is not specified, a default array ["roi_default"] will be created. The TargetROIDef object with the name "roi_default" will have a default configuration of tasks including one barcode reading task, one label recognition task, and one document normalizer task.|
