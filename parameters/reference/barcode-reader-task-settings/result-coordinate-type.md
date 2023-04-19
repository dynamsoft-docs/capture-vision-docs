---
layout: default-layout
Title: ResultCoordinateType - Dynamsoft Barcode Reader Parameters
Description: The parameter ResultCoordinateType of Dynamsoft Barcode Reader defines the returned coordinate type.
Keywords: ResultCoordinateType
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-reader-task-settings/result-coordinate-type.html
---

# ResultCoordinateType

Parameter `ResultCoordinateType` defines the returned coordinate type.

## Example

```json
{
    "ResultCoordinateType": "RCT_PIXEL"
}
```

## Parameter Summary

| ResultCoordinateType Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>One of the Candidate Modes as a string:<br>RCT_PIXEL<br>RCT_PERCENTAGE |
| **Default Value**<br>RCT_PIXEL |

## Candidate Modes Introduction

### RCT_PIXEL

Returns the coordinate in pixel value.

### RCT_PERCENTAGE

Returns the coordinate as a percentage value.
