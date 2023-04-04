---
layout: default-layout
Title: ApplicableTextLineNumbers - Dynamsoft Label Recognizer Parameters
Description: The parameter ApplicableTextLineNumbers of Dynamsoft Label Recognizer defines the line numers of the targeting text lines.
Keywords: Applicable text line numbers
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ApplicableTextLineNumbers

The line numers of the targeting lines which are specified by the `TextLineSpecification` object.

```json
{
    "ApplicableTextLineNumbers": "1-3, 5, 7-10"
}
```

| Parameter Name | ApplicableTextLineNumbers|
| ------------------- | ------------------------ |
| Type | *String* |
| Range | A string of one or more of the following data,separated by commas:<br>1. One int value which represents a specified line index;<br>2. One Expression, start index and stop index connected with ""-"", which represents a specified line index range. |
| Default Value | "" |

**Remarks**

- The value is 1-based.
- "" represents all lines.
- The processed of the not specified text lines will implement the default settings.
- If the line number you specified doesn't exist, the library will ignore it.
