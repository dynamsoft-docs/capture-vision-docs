---
layout: default-layout
Title: ImageSourceState - Dynamsoft Core Enumerations
Description: The enumeration ImageSourceState of Dynamsoft Core describes the state of ImageSourceAdapter.
Keywords: Image tag type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageSourceState
---

# Enumeration ImageSourceState

Describes the state of `ImageSourceAdapter`.

```cpp
typedef enum ImageSourceState
{
    /* The buffer of ImageSourceAdapter is temporarily empty. */
    ISS_BUFFER_EMPTY,
    /* The source of ImageSourceAdapter is empty. */
    ISS_EXHAUSTED
} ImageSourceState;
```
