---   
layout: default-layout
title: CaptureVisionTemplate - Dynamsoft Capture Vision Parameters
description: The CaptureVisionTemplate object in the Dynamsoft Capture Vision.
keywords: CaptureVisionTemplate
---

# CaptureVisionTemplate Object

A `CaptureVisionTemplate` object is the entry point of a parameter template in Dynamsoft Capture Vision (DCV) SDK.

## Example

```json
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
```

## Parameters

| Parameter Name | Type | Required/Optional | Description |
| -------------- | ---- | ----------------- | ----------- |
| [`Name`]({{site.dcvb_parameters_reference}}capture-vision-template/name.html) | String | Required | The unique identifier for this template. |
| [`ImageSourceName`]({{site.dcvb_parameters_reference}}capture-vision-template/image-source-name.html) | String | Optional | The name of the `ImageSource` object defining the input source. |
| [`ImageROIProcessingNameArray`]({{site.dcvb_parameters_reference}}capture-vision-template/image-roi-processing-name-array.html) | String Array | Optional | Array of `TargetROIDef` object names defining recognition tasks on image ROIs. |
| [`SemanticProcessingNameArray`]({{site.dcvb_parameters_reference}}capture-vision-template/semantic-processing-name-array.html) | String Array | Optional | Array of `SemanticProcessing` object names for post-processing tasks. |
| [`OutputOriginalImage`]({{site.dcvb_parameters_reference}}capture-vision-template/output-original-image.html) | Integer | Optional | Whether to output the original input image (0 or 1). |
| [`MaxParallelTasks`]({{site.dcvb_parameters_reference}}capture-vision-template/max-parallel-tasks.html) | Integer | Optional | Maximum number of parallel tasks for the DCV runtime. |
| [`MinImageCaptureInterval`]({{site.dcvb_parameters_reference}}capture-vision-template/min-image-capture-interval.html) | Integer | Optional | Minimum time interval (in milliseconds) between consecutive image captures. |
| [`Timeout`]({{site.dcvb_parameters_reference}}capture-vision-template/timeout.html) | Integer | Optional | Maximum processing time (in milliseconds) per image. |

## Input Source Configuration

The `ImageSourceName` parameter references an `ImageSource` object defining the image input source. When DCV starts capturing, it parses the `ImageSource` parameter, converts it into an [Image Source Adapter (ISA)]({{site.dcvb_architecture}}input.html#image-source-adapter) object, and continuously obtains images from it.

## Captured Output Configuration

`OutputOriginalImage`, `ImageROIProcessingNameArray`, and `SemanticProcessingNameArray` control the captured output, organized as a `CapturedResult` interface in DCV. `CapturedResult` represents a set of all captured result items on an image. Each type of result item represents the output of different task types. The following figure lists the relationship between DCV output parameters and output results.

![Relationship between DCV parameters and output result item types](assets/dcv-parameters-result-relationship.png)

**Parameter and result relationships:**
- `ImageROIProcessingNameArray` produces `BarcodeResultItem`, `TextLineResultItem`, `DetectedQuadResultItem`, and `NormalizedImageResultItem`
- `SemanticProcessingNameArray` produces `ParsedResultItem`
- `ImageROIProcessingNameArray` references one or more `TargetROIDef` objects
- `SemanticProcessingNameArray` references one or more `SemanticProcessing` objects

## Core Design of TargetROIDef Object

The [`TargetROIDef`]({{site.dcvb_parameters}}file/target-roi-definition/index.html) object specifies one or more recognition tasks to be performed on regions of interest (ROIs) within an image. In simple terms:

```
TargetROIDef = Recognition Task Definition + Spatial Location Definition
```

### Key Concepts

![An example showing the key concepts](assets/roi-concept.png)

| Concept | Description | Example Explanation |
| :------ | :---------- | :------------------ |
| **Recognition Tasks** | Tasks include barcode recognition, label recognition, document boundary detection, etc. | `ROI1` and `ROI2` are two `TargetROIDef` objects. Task `barcode_task` is configured on `ROI1` and task `label_task` is configured on `ROI2`. |
| **Atomic Result** | Atomic result of recognition task output. Can be a color detection region, barcode, text line, table cell, detected quadrilateral, etc. | `T1`, `T2`, `T3` are three `TextLineResultItem` objects, and `B1` is one `BarcodeResultItem` object. |
| **Spatial Location** | A `Location` configured on a `TargetROIDef` may generate zero or more target regions on which to perform recognition tasks. | `ROI1.Location` is `null`, generating one target region. `ROI2.Location` is an upward offset relative to `ROI1` output regions. |
| **Reference Region** | A physical quadrilateral region. Two types: **entire image region** and **atomic result region**. The former is the quadrilateral extent of the original image; the latter is the quadrilateral extent of each atomic result. | `ROI1` has one reference region (entire image). `ROI2` has three reference regions generated from `T1`, `T2`, `T3`. |
| **Target Region** | A physical quadrilateral region calculated from a reference region and offset. | `ROI1` has one target region equal to the reference region. `ROI2` has three target regions calculated by offsets from `T1`, `T2`, `T3` quadrilateral regions. |

### Workflow Design Based on Reference/Target Regions

Using recursive definition of reference relationships between `TargetROIDef` objects, complex workflows can be constructed for complex scenarios.

**Example:** Read barcodes below `P/N` and above `L/N` in the image. Positional dependencies:
- Target barcode location (blue box) can be calculated from text line locations (`P/N` and `L/N`)
- Text lines (`P/N` and `L/N`) are on the first and fifth lines inside the label border (green box)

![Sample image illustrating workflow design](assets/example2.png)

The following json is a parameter template fragment that configures ROI dependencies to solve the above problems.

```json
{
    "TargetROIDefOptions": [
        {
            "Name": "ddn_roi",
            "TaskSettingNameArray": ["ddn_task"],
            "Location": null
        },
        {
            "Name": "dlr_roi",
            "TaskSettingNameArray": ["dlr_task"],
            "Location": {
                "ReferenceObjectFilter": {
                    "ReferenceTargetROIDefNameArray": ["ddn_roi"]
                },
                "Offset": null
            }
        },
        {
            "Name": "dbr_roi1",
            "TaskSettingNameArray": ["dbr_task"],
            "Location": {
                "ReferenceObjectFilter": {
                    "ReferenceTargetROIDefNameArray": ["dlr_roi"]
                },
                "Offset": {
                    "MeasuredByPercentage": 0,
                    "ReferenceYAxis": {"AxisType": "AT_EDGE", "EdgeIndex": 2},
                    "FirstPoint": [0, 10],
                    "SecondPoint": [100, 10],
                    "ThirdPoint": [100, 50],
                    "FourthPoint": [0, 50]
                }
            }
        },
        {
            "Name": "dbr_roi2",
            "TaskSettingNameArray": ["dbr_task"],
            "Location": {
                "ReferenceObjectFilter": {
                    "ReferenceTargetROIDefNameArray": ["dlr_roi"]
                },
                "Offset": {
                    "MeasuredByPercentage": 0,
                    "ReferenceYAxis": {"AxisType": "AT_EDGE", "EdgeIndex": 0},
                    "FirstPoint": [0, -50],
                    "SecondPoint": [100, -50],
                    "ThirdPoint": [100, -10],
                    "FourthPoint": [0, -10]
                }
            }
        }
    ]
}
```

**In this configuration:**
- Four `TargetROIDef` objects: `ddn_roi`, `dlr_roi`, `dbr_roi1`, and `dbr_roi2`
- `ddn_roi` depends on the entire image region
- `dlr_roi` depends on `ddn_roi` with null offset (same region)
- `dbr_roi1` depends on `dlr_roi` with downward offset
- `dbr_roi2` depends on `dlr_roi` with upward offset

### Construct a Dependency Graph

When DCV parses `TargetROIDef` objects, it constructs a directed dependency graph based on configured dependencies. Tasks execute in the order specified by the dependency graph.

![Dependency Graph](assets/dependency-graph.png)

### Filter Out the Desired Reference Regions

In practical applications, a `TargetROIDef` may want to depend only on reference regions from another `TargetROIDef` that meet specific filtering conditions, such as text matching a regular expression or barcodes meeting a specific format requirements.

Based on the previous example, regular expression filtering conditions can be added to `dbr_roi1` and `dbr_roi2`:

```json
{
    "TargetROIDefOptions": [
        {
            "Name": "roi_dbr1",
            "TaskSettingNameArray": ["dbr_task"],
            "Location": {
                "ReferenceObjectFilter": {
                    "ReferenceTargetROIDefNameArray": ["roi_dlr"],
                    "TextLineFilteringCondition": {
                        "LineStringRegExPattern": "^P/N"
                    }
                },
                "Offset": {}
            }
        },
        {
            "Name": "roi_dbr2",
            "TaskSettingNameArray": ["dbr_task"],
            "Location": {
                "ReferenceObjectFilter": {
                    "ReferenceTargetROIDefNameArray": ["roi_dlr"],
                    "TextLineFilteringCondition": {
                        "LineStringRegExPattern": "^L/N"
                    }
                },
                "Offset": {}
            }
        }
    ]
}
```

**Filtering logic:**
- `roi_dbr1` depends only on regions from `roi_dlr` where text matches pattern `^P/N`
- `roi_dbr2` depends only on regions from `roi_dlr` where text matches pattern `^L/N`
- Reference regions not meeting filter criteria are discarded

For more details about filtering reference objects, refer to [`ReferenceObjectFilter`]({{site.dcvb_parameters_reference}}target-roi-def/location.html#referenceobjectfilter).

## Core Design of SemanticProcessing Object

The [`SemanticProcessing`]({{site.dcvb_parameters}}file/semantic-processing/index.html) object specifies tasks to analyze and extract information from image ROI processing results. The workflow involves the following concepts:

### Prerequisites

A `SemanticProcessing` object takes effect when its name is referenced in `CaptureVisionTemplate.SemanticProcessingNameArray`.

### Launch Timing

The semantic process triggers only after all recognition tasks referenced in `CaptureVisionTemplate.ImageROIProcessingNameArray` have been completed.

### Data Filtering

Data filtering selects relevant sources, such as label text matching a specific regular expression or barcodes meeting a specific format. Use `ReferenceObjectFilter` to specify data filtering criteria.

### Task Execution

This is the main part of the workflow where actual tasks are defined. Use `TaskSettingNameArray` to specify tasks by referencing a [`CodeParserTaskSetting`]({{site.dcvb_parameters}}file/task-settings/code-parser-task-settings.html) object name.

### Results Reporting

Currently, semantic-processing supports code parsing tasks. Results are returned with the `OnParsedResultsReceived` callback.