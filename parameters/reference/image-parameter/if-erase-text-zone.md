---
layout: default-layout
title: IfEraseTextZone - Dynamsoft Capture Vision Parameters
description: The parameter IfEraseTextZone of Dynamsoft Capture Vision is for controlling whether to erase the detected text zone.
keywords: IfEraseTextZone, parameter reference, parameter
---


# IfEraseTextZone

Parameter `IfEraseTextZone` sets whether to erase the detected text zone. The detected text zone is the result of text detection process when enables `TextDetectionMode`.

## Example

```json
{
    "IfEraseTextZone": 1
}
```

## Parameter Details

| IfEraseTextZone Parameter Details |
| :---------------------------------- |
| **Description**<br>0: Do not erase the text zone.<br>1: Erase the text zone. |
| **Type**<br>*int* |
| **Value range**<br>[0, 1] |

>Note: Do not erase text when a text recognition task is to be performed.

### Default Setting

If the `IfEraseTextZone` is not configured in your template file, the following settings will be used as the default settings.

#### For Barcode Decoding

```json
{
    "IfEraseTextZone": 1
}
```

#### For Label Recognizing

```json
{
    "IfEraseTextZone": 0
}
```

#### For Document Normalizing

```json
{
    "IfEraseTextZone": 0
}
```
