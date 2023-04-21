---
layout: default-layout
Title: AustralianPostEncodingTable - Dynamsoft Barcode Reader Parameters
Description: This page shows Dynamsoft Barcode Reader Parameter Reference for AustralianPostEncodingTable.
Keywords: AustralianPostEncodingTable, parameter reference, parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /parameters/reference/barcode-format-specification/australian-post-encoding-table.html
---

# AustralianPostEncodingTable

`AustralianPostEncodingTable` helps specify the encoding table used to code the Customer Information Field of Australian Post Customer Barcode.
## Example

```json
{
    "AustralianPostEncodingTable": "N"
}
```

## Parameter Summary

The structure of the `AustralianPostEncodingTable` is shown as follow:

| AustralianPostEncodingTable Parameter Summary |
| :--------------------------------- |
| **Type**<br>*string* |
| **Range**<br>"C"<br>"N" |
| **Default Value**<br>"C" |

### Default Settings

If the `AustralianPostEncodingTable` is not configured in your template file, the following settings will be used as the default settings.

```json
{
    "AustralianPostEncodingTable": "C"
}
```
