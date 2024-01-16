---
layout: default-layout
title: ConcatResults - Dynamsoft Label Recognizer Parameters
description: The parameter ConcatResults defines whether to concatenate the output results of the TextLineSpecification object.
keywords: top-level object, ConcatResults
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/text-line-specification/concat-results.html
---

# ConcatResults

Parameter `ConcatResults` defines whether to concatenate multiple lines of text. For example, if two lines of text are recognized in a label, the results will be concatenated into one line using `ConcatSeparator` as the separator.

## Example

```json
{
    "Name": "tls_0",
    "ConcatResults" : 0
}
```

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*int* |
| **Range**<br>0,1 |
| **Default Value**<br>0. It does not concat the text line result for the `TextLineSpecification` object. |
