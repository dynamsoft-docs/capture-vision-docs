---
layout: default-layout
title: ImageROIProcessingNameArray - Dynamsoft Capture Vision Parameters
description: The parameter ImageROIProcessingNameArray of Dynamsoft Capture Vision defines the collection of image ROI processing object names.
keywords: image ROI processing, TargetROIDef, CaptureVisionTemplate
permalink: /parameters/reference/capture-vision-template/image-roi-processing-name-array.html
---
# ImageROIProcessingNameArray

Parameter `ImageROIProcessingNameArray` defines the collection of image ROI processing object names, used to refer to the `TargetROIDef` objects

## JSON Structure

**Location in template:**
```
CaptureVisionTemplates[i]
    └── ImageROIProcessingNameArray
```

**Parent object:** [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object

**Example:**

```json
{
    "ImageROIProcessingNameArray": ["dlr_roi"]
}
```

> [!NOTE]
> - This snippet shows only the `ImageROIProcessingNameArray` parameter.
> - To use it, embed this parameter within a [CaptureVisionTemplate]({{ site.dcvb_parameters }}file/capture-vision-template.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| ImageROIProcessingNameArray Parameter Details |
| :----------------------------------- |
| **Type**<br>*String[]* |
| **Range**<br>Each element is the name of a `TargetROIDef` object. |
| **Default Value**<br>['roi_default'] |
| **Remarks**<br>If `ImageROIProcessingNameArray` is not specified, a default array ["roi_default"] will be created. The TargetROIDef object with the name "roi_default" will have a default configuration of tasks including one barcode reading task, one label recognition task, and one document normalizer task.|
