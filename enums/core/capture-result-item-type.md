---
layout: default-layout
Title: CapturedResultItemType - Dynamsoft Core Enumerations
Description: The enumeration CapturedResultItemType of Dynamsoft Core describes all types of captured result item.
Keywords: Captured result types
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CapturedResultItemType
---

# Enumeration CapturedResultItemType

`CapturedResultItemType` describes all types of captured result item.

```cpp
typedef enum CapturedResultItemType
{
    /** The type of the CapturedResultItem is "raw image". */
    CRIT_RAW_IMAGE = 1,
    /** The type of the CapturedResultItem is "barcode". */
    CRIT_BARCODE = 2,
    /** The type of the CapturedResultItem is "text line". */
    CRIT_TEXT_LINE = 4,
    /** The type of the CapturedResultItem is "detected quad". */
    CRIT_DETECTED_QUAD = 8,
    /** The type of the CapturedResultItem is "normalized image". */
    CRIT_NORMALIZED_IMAGE = 16,
    /** The type of the CapturedResultItem is "parsed result". */
    CRIT_PARSED_RESULT = 32
} CapturedResultItemType;
```
