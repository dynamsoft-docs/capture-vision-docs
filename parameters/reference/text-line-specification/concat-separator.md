---
layout: default-layout
title: ConcatSeparator - Dynamsoft Label Recognizer Parameters
description: The parameter ConcatSeparator defines the concat separator of the TextLineSpecification object.
keywords: top-level object, ConcatSeparator
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
permalink: /parameters/reference/text-line-specification/concat-separator.html
---

# ConcatSeparator

Parameter `ConcatSeparator` defines the concat separator used to join multiple lines of text. For example, if two lines of text are recognized in a label, the results will be concatenated into one line using `ConcatSeparator` as the separator.

## Example

```json
{
    "Name": "tls_0",
    "ConcatSeparator" : "\n"
}
```

## Parameter Summary

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>"\n". It represents the connection separator that joins text.|
