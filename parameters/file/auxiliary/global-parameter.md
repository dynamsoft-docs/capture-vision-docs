---
layout: default-layout
title: GlobalParameters - Dynamsoft Capture Vision Parameter File
description: The GlobalParameters object in the Dynamsoft Capture Vision Parameter File defines the global parameters.
keywords: image dimension, global parameters
needAutoGenerateSidebar: true
noTitleIndex: true
---

# GlobalParameter Object

A `GlobalParameter` object defines the global parameters for Dynamsoft Capture Vision. The available global parameters are listed below.

## Example

```json
{
    "GlobalParameter":{
        "MaxTotalImageDimension": 0,
        "IntraOpNumThreads": 0
    }
}
```

## Available Parameters

### MaxTotalImageDimension

Defines the maximum value of total dimension (in million pixel) of source images the library can process concurrently.

| Parameter Summary |
| :---------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 0x7fffffff] |
| **Default Value**<br>0 |
| **Remarks**<br>0 means no limitation. |

### IntraOpNumThreads

Sets the global number of threads used internally for model execution.

| Parameter Summary |
| :---------------- |
| **Type**<br>*int* |
| **Range**<br>[0, 256] |
| **Default Value**<br>4 |
| **Remarks**<br>0 means the library automatically decides the number of threads to use based on the system's CPU core count. |

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.
