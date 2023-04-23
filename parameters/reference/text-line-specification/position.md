---
layout: default-layout
Title: Text Line Area Points - Dynamsoft Label Recognizer Parameters
Description: The parameter Text Line Area Points of Dynamsoft Label Recognizer defines how to normalize the characters.
Keywords: Character normalization
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/text-line-specification/position.html
---

# Text Line Area Points

Text line area points parameters defines the position of the text lines with the vertice points. The point coordinates are measured in percentage based on the size of the `TargetROI`.

## Example

```json
{
    "FirstPoint" : [ 0, 0 ],
    "SecondPoint" : [ 100, 0 ],
    "ThirdPoint" : [ 100, 20 ],
    "FourthPoint" : [ 0, 20 ]
}
```

Only the text lines that located in this area will be processed.

## Parameter Summary

### FirstPoint

The top-left vertex coordinate of the the text line. The coordinate is measured in percentage.

| FirstPoint Parameter Summary |
| :------------------------ |
| **Type**<br>*int[2]* |
| **Range**<br>Each member of the array should be a int value between 0 to 100. |
| **Default Value**<br>*null* |

### SecondPoint

The top-right vertex coordinate of the the text line. The coordinate is measured in percentage.

| SecondPoint Parameter Summary |
| :---------------------------- |
| **Type**<br>*int[2]* |
| **Range**<br>Each member of the array should be a int value between 0 to 100. |
| **Default Value**<br>*null* |

### ThirdPoint

The bottom-right vertex coordinate of the the text line. The coordinate is measured in percentage.

| ThirdPoint Parameter Summary |
| :--------------------------- |
| **Type**<br>*int[2]* |
| **Range**<br>Each member of the array should be a int value between 0 to 100. |
| **Default Value**<br>*null* |

### FourthPoint

The bottom-left vertex coordinate of the the text line. The coordinate is measured in percentage.

| FourthPoint Parameter Summary |
| :---------------------------- |
| **Type**<br>*int[2]* |
| **Range**<br>Each member of the array should be a int value between 0 to 100. |
| **Default Value**<br>*null* |
