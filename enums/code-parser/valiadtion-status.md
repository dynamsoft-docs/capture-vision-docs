---
layout: default-layout
Title: ValidationStatus - Dynamsoft Code Parser Enumerations
Description: The enumeration ValidationStatus of Dynamsoft Code Parser describes the validation status of a parsed field.
Keywords: Validation status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ValidationStatus
---

# Enumeration ValidationStatus

`ValidationStatus` describes the validation status of a parsed field.

```cpp
typedef enum ValidationStatus
{
    /** The field has no validation specified. */
    VS_NONE,
    /** The validation for the field has been succeeded. */
    VS_SUCCEEDED,
    /** The validation for the field has been failed. */
    VS_FAILED
} ValidationStatus;
```
