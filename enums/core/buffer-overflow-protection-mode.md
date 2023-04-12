---
layout: default-layout
Title: BufferOverflowProtectionMode - Dynamsoft Core Enumerations
Description: The enumeration BufferOverflowProtectionMode of Dynamsoft Core describes the protection modes when the buffer of ImageSourceAdapter is overflow.
Keywords: Buffer overflow protection mode 
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BufferOverflowProtectionMode
---

# Enumeration BufferOverflowProtectionMode

Describes the protection modes when the buffer of `ImageSourceAdapter` is overflow.

```cpp
typedef enum BufferOverflowProtectionMode
{
    /** New images are blocked when the buffer is full.*/
    BOPM_BLOCK, // = 0,
    /** New images are appended at the end, and oldest images are pushed out from the beginning if the buffer is full.*/
    BOPM_APPEND // = 1,
} BufferOverflowProtectionMode;
```
