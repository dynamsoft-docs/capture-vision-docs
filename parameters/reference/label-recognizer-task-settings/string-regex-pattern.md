---
layout: default-layout
Title: StringRegExPattern - Dynamsoft Label Recognizer Parameters
Description: The parameter StringRegExPattern of Dynamsoft Label Recognizer defines the regular expression pattern for concatenated strings of recognized text lines.
Keywords: text lines, concatenated strings, regular expression
needAutoGenerateSidebar: true
noTitleIndex: true
---

# StringRegExPattern

Specifies the regular expression pattern for concatenated strings of recognized text lines.

```json
{
    "StringRegExPattern" : ""
}
```

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>All standard regular expressions.|
| **Default Value**<br>"" |
| **Remarks**<br>This is a filtering parameter. After all recognized text lines are concatenated, they will be matched against this regular expression. Results that do not match will not be output.|
