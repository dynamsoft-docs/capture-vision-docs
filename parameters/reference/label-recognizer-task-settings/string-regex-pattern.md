---
layout: default-layout
title: StringRegExPattern - Dynamsoft Label Recognizer Parameters
description: The parameter StringRegExPattern of Dynamsoft Label Recognizer defines the regular expression pattern for concatenated strings of recognized text lines.
keywords: text lines, concatenated strings, regular expression
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/label-recognizer-task-settings/string-regex-pattern.html
---

# StringRegExPattern

Parameter `StringRegExPattern` specifies the regular expression pattern for concatenated strings of recognized text lines.

## Example

```json
{
    "StringRegExPattern" : ""
}
```

## Parameter Summary

| StringRegExPattern Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>All standard regular expressions.|
| **Default Value**<br>"" |
| **Remarks**<br>This is a filtering parameter. After all recognized text lines are concatenated, they will be matched against this regular expression. Results that do not match will not be output. |
