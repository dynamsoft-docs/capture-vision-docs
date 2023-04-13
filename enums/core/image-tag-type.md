---
layout: default-layout
Title: ImageTagType - Dynamsoft Core Enumerations
Description: The enumeration ImageTagType of Dynamsoft Core describes the types of image tags.
Keywords: Image tag type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageTagType
---

# Enumeration ImageTagType

Describes the type of the image tag, which is used to distinguish video frame and file images.

```cpp
typedef enum ImageTagType
{
    /** The image is a file image. */
    ITT_FILE_IMAGE,
    /** The image is a video frame. */
    ITT_VIDEO_FRAME
} ImageTagType;
```
