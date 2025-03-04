---
layout: default-layout
title: ClusterSamplesCountThreshold - Dynamsoft Label Recognizer Parameters
description: The parameter ClusterSamplesCountThreshold of Dynamsoft Label Recognizer defines the threshold for successful character clustering.
keywords: confusable character clustering
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
---

# ClusterSamplesCountThreshold

The parameter `ClusterSamplesCountThreshold` defines the threshold for successful character clustering. It defines the minimum number of samples in a single cluster. If every character in a group of confusable characters has been successfully clustered, the group will stop clustering. For example, [0,O,o] is a typical group of confusing characters.

## Example

```json
{
    "ClusterSamplesCountThreshold": 5
}
```

## Parameter Summary

| ClusterSamplesCountThreshold Parameter Summary |
| :----------------------------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7FFFFFFF].|
| **Default Value**<br>0 |
| **Remarks**<br>0 indicates that the confusable characters clustering is not enabled.|
