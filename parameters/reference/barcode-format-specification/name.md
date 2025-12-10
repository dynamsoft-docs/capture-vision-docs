---
layout: default-layout
title: Name - Dynamsoft Capture Vision Parameter Reference BarcodeFormatSpecification Object.
description: The parameter Name defines the unique identifier of BarcodeFormatSpecification object.
keywords: top-level object, name, unique identifier
---

# Name

Parameter `Name` represents the name of a `BarcodeFormatSpecification` object, which serves as its unique identifier.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── Name
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "Name" : "bf_0"
}
```

> [!NOTE]
> - This snippet shows only the `Name` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Parameter Details |
| :----------------------------------- |
| **Type**<br>*String* |
| **Default Value**<br>It must be a mandatory setting value. |
| **Remarks**<br>It must be a unique name. |
