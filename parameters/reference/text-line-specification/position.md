---
layout: default-layout
title: Text Line Area Points - Dynamsoft Label Recognizer Parameters
description: The parameter Text Line Area Points of Dynamsoft Label Recognizer defines how to normalize the characters.
keywords: Character normalization
---

# Text Line Area Points

Text line area points parameters defines the position of the text lines with the vertices points. The point coordinates are measured in percentage based on the size of the `TargetROI`. Only the text lines that located in this area will be processed.

## JSON Structure

**Location in template:**
```
TextLineSpecificationOptions[i]
    └── FirstPoint
    └── SecondPoint
    └── ThirdPoint
    └── FourthPoint
```

**Parent object:** [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object

**Example:**

```json
{
    "FirstPoint": [ 0, 0 ],
    "SecondPoint": [ 100, 0 ],
    "ThirdPoint": [ 100, 20 ],
    "FourthPoint": [ 0, 20 ]
}
```

> [!NOTE]
> - This snippet shows only the `Position` parameter.
> - To use it, embed this parameter within a [TextLineSpecification]({{ site.dcvb_parameters }}file/auxiliary/text-line-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)


## Parameter Details

### FirstPoint

The top-left vertex coordinate of the the text line. The coordinate is measured in percentage.

| FirstPoint Parameter Details |
| :------------------------ |
| **Type**<br>*int[2]* |
| **Range**<br>Each member of the array should be a int value between 0 to 100. |
| **Default Value**<br>*null* |

### SecondPoint

The top-right vertex coordinate of the the text line. The coordinate is measured in percentage.

| SecondPoint Parameter Details |
| :---------------------------- |
| **Type**<br>*int[2]* |
| **Range**<br>Each member of the array should be a int value between 0 to 100. |
| **Default Value**<br>*null* |

### ThirdPoint

The bottom-right vertex coordinate of the the text line. The coordinate is measured in percentage.

| ThirdPoint Parameter Details |
| :--------------------------- |
| **Type**<br>*int[2]* |
| **Range**<br>Each member of the array should be a int value between 0 to 100. |
| **Default Value**<br>*null* |

### FourthPoint

The bottom-left vertex coordinate of the the text line. The coordinate is measured in percentage.

| FourthPoint Parameter Details |
| :---------------------------- |
| **Type**<br>*int[2]* |
| **Range**<br>Each member of the array should be a int value between 0 to 100. |
| **Default Value**<br>*null* |
