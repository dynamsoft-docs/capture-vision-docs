---
layout: default-layout
title: AustralianPostEncodingTable - Dynamsoft Barcode Reader Parameters
description: The parameter AustralianPostEncodingTable of Dynamsoft Barcode Reader helps specify the encoding table used to code the Customer Information Field of Australian Post Customer Barcode.
keywords: AustralianPostEncodingTable, parameter reference, parameter
---

# AustralianPostEncodingTable

Parameter `AustralianPostEncodingTable` helps specify the encoding table used to code the Customer Information Field of Australian Post Customer Barcode.

## JSON Structure

**Location in template:**
```
BarcodeFormatSpecificationOptions[i]
    └── AustralianPostEncodingTable
```

**Parent object:** [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object

**Example:**

```json
{
    "AustralianPostEncodingTable": "N"
}
```

> [!NOTE]
> - This snippet shows only the `AustralianPostEncodingTable` parameter.
> - To use it, embed this parameter within a [BarcodeFormatSpecification]({{ site.dcvb_parameters }}file/auxiliary/barcode-format-specification.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

The structure of the `AustralianPostEncodingTable` is shown as follow:

| AustralianPostEncodingTable Parameter Details |
| :--------------------------------- |
| **Type**<br>*String* |
| **Range**<br>"C" or "N" |
| **Default Value**<br>"C" |
