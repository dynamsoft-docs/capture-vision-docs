---   
layout: default-layout
title: ApplicableTextLineNumbers - Dynamsoft Capture Vision TextLineSpecification parameter
description: This page introduce how to set TextLineSpecification parameter ApplicableTextLineNumbers.
keywords: Applicable text line numbers
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ApplicableTextLineNumbers

Specify which lines in the ROI will apply the `TextLineSpecification` settings.

```json
{
    "ApplicableTextLineNumbers": "1-3, 5, 7-10"
}
```

| Json Parameter Name | ApplicableTextLineNumbers|
| ------------------- | ------------------------ |
| Type | *String* |
| Range | A string of one or more of the following data,separated by commas:<br>1. One int value which represents a specified line index;<br>2. One Expression, start index and stop index connected with ""-"", which represents a specified line index range; |
| Default Value | "" |

| Json Parameter Name | Value Type | Value Range | Default Value |
| ------------------- | ---------- | ----------- | ------------- |
| ApplicableTextLineNumbers | *string* | A string of one or more of the following data,separated by commas:<br>1. One int value which represents a specified line index;<br>2. One Expression, start index and stop index connected with ""-"", which represents a specified line index range; | "" |
