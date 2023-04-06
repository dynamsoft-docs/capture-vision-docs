---
layout: default-layout
Title: ContentType - Dynamsoft Document Normalizer Parameters
Description: The parameter ContentType of Dynamsoft Document Normalizer is XXX.
Keywords:
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ContentType

Parameter `ContentType` defines which contents are the targeting objects. Currently, the supported contents are:

- Document pages
- Table

```json
{
    "ContentType": "CT_TABLE"
}
```

| Parent Object | DocumentNormalizerTaskSetting |
| :------------ | :---------------------------- |
| Parameter Name | ContentType |
| **Type** | *String* |
| Range | "CT_DOCUMENT", "CT_TABLE" or "CT_UNKNOWN". |
| Default Value | "CT_DOCUMENT" |
