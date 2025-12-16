---
layout: default-layout
title: ClusterSamplesCountThreshold - Dynamsoft Label Recognizer Parameters
description: The parameter ClusterSamplesCountThreshold of Dynamsoft Label Recognizer defines the threshold for successful character clustering.
keywords: confusable character clustering
---

# ClusterSamplesCountThreshold

The parameter `ClusterSamplesCountThreshold` defines the threshold for successful character clustering. It defines the minimum number of samples in a single cluster. If every character in a group of confusable characters has been successfully clustered, the group will stop clustering. For example, [0,O,o] is a typical group of confusing characters.

## JSON Structure

**Location in template:**

```
LabelRecognizerTaskSettingOptions[i]
    └── SectionArray[j] (Section object)
        └── StageArray[k] (Stage object where Stage = "SST_RECOGNIZE_RAW_TEXT_LINES")
            └── ClusterSamplesCountThreshold
```

**Parent object:** [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html)

**Example:**

```json
{
    "ClusterSamplesCountThreshold": 5
}
```

> [!NOTE]
> - This snippet shows only the `ClusterSamplesCountThreshold` parameter.
> - To use it, embed this parameter within a [RecognizeRawTextLinesStage]({{ site.dcvb_parameters }}reference/label-recognizer-task-settings/stage-recognize-raw-text-lines.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json)

## Parameter Details

| ClusterSamplesCountThreshold Parameter Details |
| :----------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7FFFFFFF].|
| **Default Value**<br>0 |
| **Remarks**<br>0 indicates that the confusable characters clustering is not enabled.|
