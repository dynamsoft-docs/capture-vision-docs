---
layout: default-layout
title: StringRegExPattern - Dynamsoft Capture Vision Text Line Specification Parameters
description: The parameter StringRegExPattern of text line specification is for specifying the regex pattern of the text line strings.
keywords: string length range, parameter reference, parameter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# StringRegExPattern

Specifies the regular expression pattern of the string within a line.  

## Example

```json
{
    "LineStringRegExPattern":""
}
```

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>All standard regular expressions.|
| **Default Value**<br>"" |
| **Remarks**<br>This is a filtering parameter. After all recognized text lines are concatenated, they will be matched against this regular expression. Results that do not match will not be output. |
