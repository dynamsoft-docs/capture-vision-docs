---
layout: default-layout
Title: ImageCaptureDistanceMode - Dynamsoft Core Enumerations
Description: The enumeration ImageCaptureDistanceMode of Dynamsoft Core is used to distinguish the close-up images from the prospect images.
Keywords: Image capture distance
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageCaptureDistanceMode
---

# Enumeration ImageCaptureDistanceMode

`ImageCaptureDistanceMode` describes the shooting mode of the image. It is used in the `overlap` mode of `Panorama`.

```cpp
typedef enum ImageCaptureDistanceMode 
{
    /** The image is taken by close-up shot camera. */
    ICDM_NEAR,    
    /** The image is taken by long shot camera. */
    ICDM_FAR
} CaptureDistanceMode;
```
