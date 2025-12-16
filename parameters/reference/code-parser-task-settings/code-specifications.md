---
layout: default-layout
title: CodeSpecifications - Dynamsoft Capture Vision Parameter Reference
description: The parameter CodeSpecifications of Dynamsoft Capture Vision. 
noTitleIndex: true
---
# CodeSpecifications

Parameter `CodeSpecifications` specifies the names of `CodeSpecification` used for code parsing.

## JSON Structure

**Location in template:**
```
CodeParserTaskSettingOptions[i]
    └── CodeSpecifications
```

**Parent object:** [CodeParserTaskSetting]({{ site.dcvb_parameters }}file/task-settings/code-parser-task-settings.html) object

**Example:**

```json
{
    "CodeSpecifications" : ["VIN"]
}
```

> [!NOTE]
> - This snippet shows only the `CodeSpecifications` parameter.
> - To use it, embed this parameter within a [CodeParserTaskSetting]({{ site.dcvb_parameters }}file/task-settings/code-parser-task-settings.html) object.
> - For the complete JSON structure, see:
>   - [Full JSON Structure]({{ site.dcvb_parameters }}file/index.html#full-json-structure)
>   - [Minimal Valid JSON]({{ site.dcvb_parameters }}file/index.html#minimal-valid-json-example)

## Parameter Details

| Brightness Parameter Details |
| :------------- |
| **Type**<br>*string array* |
| **Range**<br>Any valid string |
| **Default Value**<br>[] |

**Remarks**

- The default value, [], means all `CodeSpecification` under default resources path will be used.
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
