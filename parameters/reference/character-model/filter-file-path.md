---
layout: default-layout
title: FilterFilePath - Dynamsoft Label Recognizer Parameters
description: The parameter FilterFilePath defines a path when the library recognize characters.
keywords: Directory path
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/character-model/filter-file-path.html
---

# FilterFilePath

Parameter `FilterFilePath` defines the full path of the filter file which specifies the characters to be recognized.

## Example

```json
{
    "FilterFilePath" : "D:\\CharacterModel\\"
}
```

## Parameter Summary

| FilterFilePath Parameter Summary |
| :------------- |
| **Type**<br>*string* |

### Default Settings

If the `FilterFilePath` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "FilterFilePath" : ""
}
```
