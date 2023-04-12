---
layout: default-layout
Title: RegionObjectElementType - Dynamsoft Core Enumerations
Description: The enumeration RegionObjectElementType of Dynamsoft Core describes the types of RegionObjectElement.
Keywords: Region object element type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RegionObjectElementType
---

# Enumeration RegionObjectElementType

Describes the types of `RegionObjectElement`. 

```cpp
typedef enum RegionObjectElementType
{
    ROET_PREDETECTED_REGION,
    ROET_LOCALIZED_BARCODE,
    ROET_DECODED_BARCODE,
    ROET_LOCALIZED_TEXT_LINE,
    ROET_RECOGNIZED_TEXT_LINE,
    ROET_DETECTED_QUAD,
    ROET_NORMALIZED_IMAGE,
    ROET_SOURCE_IMAGE,
    ROET_TARGET_ROI
} RegionObjectElementType;
```
