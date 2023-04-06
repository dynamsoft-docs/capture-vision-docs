---
layout: default-layout
Title: {} - Dynamsoft Label Recognizer Parameters
Description: The parameter {} of Dynamsoft Label Recognizer defines how to normalize the characters.
Keywords: Character normalization
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Text Line Area Points

Set the position of the text lines with the vertice points. The point coordinates are measured in percentage based on the size of the `TargetROI`.

```json
{
    "FirstPoint" : [ 0, 0 ],
    "SecondPoint" : [ 100, 0 ],
    "ThirdPoint" : [ 100, 20 ],
    "FourthPoint" : [ 0, 20 ]
}
```

Only the text lines that located in this area will be processed.

## FirstPoint

The top-left vertex coordinate of the the text line. The coordinate is measured in percentage.

|  |  |
| :------------------- | :------------------------ |
| Parameter Name | FirstPoint |
| **Type** | *int Array* |
| **Range** | Each member of the array should be a int value between 0 to 100. |
| **Default Value** | *null* |

## SecondPoint

The top-right vertex coordinate of the the text line. The coordinate is measured in percentage.

|  |  |
| :------------------- | :------------------------ |
| Parameter Name | SecondPoint |
| **Type** | *int Array* |
| **Range** | Each member of the array should be a int value between 0 to 100. |
| **Default Value** | *null* |

## ThirdPoint

The bottom-right vertex coordinate of the the text line. The coordinate is measured in percentage.

|  |  |
| :------------------- | :------------------------ |
| Parameter Name | ThirdPoint |
| **Type** | *int Array* |
| **Range** | Each member of the array should be a int value between 0 to 100. |
| **Default Value** | *null* |

## FourthPoint

The bottom-left vertex coordinate of the the text line. The coordinate is measured in percentage.

|  |  |
| :------------------- | :------------------------ |
| Parameter Name | FourthPoint |
| **Type** | *int Array* |
| **Range** | Each member of the array should be a int value between 0 to 100. |
| **Default Value** | *null* |
