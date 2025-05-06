---
layout: default-layout
title: CodeSpecifications - Dynamsoft Capture Vision Parameter Reference
description: The parameter CodeSpecifications of Dynamsoft Capture Vision. 
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
---

# CodeSpecifications

Parameter `CodeSpecifications` specifies the names of `CodeSpecification` used for code parsing.

## Example

```json
{
    "CodeSpecifications" : ["VIN"]
}
```

## Parameter Summary

| Brightness Parameter Summary |
| :------------- |
| **Type**<br>*string array* |
| **Range**<br>Any valid string |
| **Default Value**<br>[] |

**Remarks**

- The default value, [], means all CodeSpecification under resources path will be used.
- A `CodeSpecification` is a file named as [Name].dcpres which defines the fields and parsing rules for a specific code type.
- Currently supported values:
    * MRTD_TD1_ID
    * MRTD_TD2_ID
    * MRTD_TD2_VISA
    * MRTD_TD3_PASSPORT
    * MRTD_TD3_VISA
    * MRTD_TD2_FRENCH_ID
    * AAMVA_DL_ID
    * AAMVA_DL_ID_WITH_MAG_STRIPE
    * SOUTH_AFRICA_DL
    * AADHAAR
    * VIN
    * GS1_AI
