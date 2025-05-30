---
layout: default-layout
title: RawTextLineStatus - Dynamsoft LabelRecognizer Enumerations
description: The enumeration RawTextLineStatus of Dynamsoft LabelRecognizer describes the final status of a raw text line.
keywords: Raw Text Line Status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RawTextLineStatus
codeAutoHeight: true
---

# Enumeration RawTextLineStatus

`RawTextLineStatus` enumerates the final status of a raw text line.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- C++
   >- Python
   >
>
```javascript
enum EnumRawTextLineStatus
{
    /** Localized but recognition not performed. */
    RTLS_LOCALIZED = 0 ,
    /** Recognition failed. */
    RTLS_RECOGNITION_FAILED = 1,
    /** Successfully recognized. */
    RTLS_RECOGNITION_SUCCEEDED = 2
}
```
>
```cpp
typedef enum RawTextLineStatus
{
    /** Localized but recognition not performed. */
    RTLS_LOCALIZED,
    /** Recognition failed. */
    RTLS_RECOGNITION_FAILED,
    /** Successfully recognized. */
    RTLS_RECOGNITION_SUCCEEDED
} RawTextLineStatus;
```
>
```python
class EnumRawTextLineStatus(IntEnum):
    # Localized but recognition not performed.
    RTLS_LOCALIZED
    # Recognition failed.
    RTLS_RECOGNITION_FAILED
    # Successfully recognized.
    RTLS_RECOGNITION_SUCCEEDED
```
