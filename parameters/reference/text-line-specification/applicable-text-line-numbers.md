---
layout: default-layout
Title: ApplicableTextLineNumbers - Dynamsoft Label Recognizer Parameters
Description: The parameter ApplicableTextLineNumbers of Dynamsoft Label Recognizer defines the line numers of the targeting text lines.
Keywords: Applicable text line numbers
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/text-line-specification/applicable-text-line-numbers.html
---

# ApplicableTextLineNumbers

The line numers of the targeting lines which are specified by the `TextLineSpecification` object.

## Example

```json
{
    "ApplicableTextLineNumbers": "1-3, 5, 7-10"
}
```

## Parameter Summary

| ApplicableTextLineNumbers Parameter Summary |
| :----------------------------------- |
| **Type**<br>*String* |
| **Range**<br>A string of one or more of the following data,separated by commas:<br>1. One int value which represents a specified line index;<br>2. One Expression, start index and stop index connected with ""-"", which represents a specified line index range. |
| **Default Value**<br>"" |
| **Remarks**<br>(1) The value is 1-based.<br>(2) "" represents all lines.<br>(3) The processed of the not specified text lines will implement the default settings.<br>(4) If the line number you specified doesn't exist, the library will ignore it. |
