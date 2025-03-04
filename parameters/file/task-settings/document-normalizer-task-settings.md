---
layout: default-layout
title: DocumentNormalizerTaskSetting - Dynamsoft Capture Vision Parameter File
description: The DocumentNormalizerTaskSetting object in the Dynamsoft Capture Vision Parameter File. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
---

# DocumentNormalizerTaskSetting Object

The `DocumentNormalizerTaskSetting` object is used to configure settings for a document normalizer task to be performed on certain regions of interest (ROIs) in an image.

```json
{
    "Name": "ddn_task_default",
    "MaxThreadsInOneTask": 4,
	"ExpectedDocumentsCount": 1,
    "BaseDocumentNormalizerTaskSettingName": "",
    "SectionArray": [
        {
            "Section": "ST_REGION_PREDETECTION",
            "ImageParameterName": "ip_default",
			"StageArray": [
				{
					"Stage": "SST_PREDETECT_REGIONS",
					"RegionPredetectionModes": [
					]
				}
			]
        },
        {
            "Section": "ST_DOCUMENT_DETECTION",
            "ContentType": "CT_DOCUMENT",
            "ImageParameterName": "ip_default",
			"StageArray": [
				{
					"Stage": "SST_ASSEMBLE_LONG_LINES"
				},
				{
					"Stage": "SST_ASSEMBLE_LOGICAL_LINES"
				},						
				{
					"Stage": "SST_DETECT_CORNERS",
					"CornerAngleRange": {
						"MaxValue": 110,
						"MinValue": 70
					}
				},
				{
					"Stage": "SST_DETECT_EDGES"
				},
				{
					"Stage": "SST_DETECT_QUADS",
					"QuadrilateralDetectionModes": [
						{
							"Mode": "QDM_GENERAL"
						}
					]
				}
			]					
        },
        {
            "Section": "ST_DOCUMENT_DESKEWING",
            "ImageParameterName": "ip_default",
			"StageArray":[
				{
					"Stage": "SST_DESKEW_IMAGE",
					"DeskewMode": {
						"ContentDirection": 0,
						"Mode": "DSM_PERSPECTIVE_CORRECTION"
					},
					"PageSize": [
						-1,
						-1
					]							
				}
			]
        },
        {
            "Section": "ST_IMAGE_ENHANCEMENT",
            "ImageParameterName": "ip_0",
			"StageArray":[
				{
					"Stage": "SST_ENHANCE_IMAGE",
					"ColourMode": "ICM_COLOUR",
					"Brightness": 0,
					"Contrast": 0							
				}
			]
        }
    ]
}
```

<div align="center">
   <p>Example 1 – Parameters of DocumentNormalizerTaskSetting</p>
</div>

## Summary of DocumentNormalizerTaskSetting top-level parameters

| Parameter Name | Description |
| -------------- | ----------- |
| [`Name`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/name.html) | Defines the name of a `DocumentNormalizerTaskSetting` object, which serves as its unique identifier. |
| [`BaseDocumentNormalizerTaskSettingName`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/base-document-normalizer-task-setting-name.html) | Represents the name of another `DocumentNormalizerTaskSetting` object to inherit from. |
| [`MaxThreadsInOneTask`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/max-threads-in-one-task.html) | Defines the maximum threads that can be consumed in one task. |
| [`ExpectedDocumentsCount`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/expected-documents-count.html) | Defines the number of documents expected to be detected. |
| [`SectionArray`]({{site.dcvb_parameters_reference}}document-normalizer-task-settings/section-array.html) | Defines which sections exist under the `DocumentNormalizerTaskSetting`. |
