---
layout: default-layout
title: ImageColourMode - Dynamsoft Document Normalizer Enumerations
description: The enumeration ImageColourMode of Dynamsoft Document Normalizer describes the mapping status of a parsed field.
keywords: Mapping status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageColourMode
---

# Enumeration ImageColourMode

`ImageColourMode` describes the output colour mode of the normalized image.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Swift
   >- C++
   >
>
```javascript
enum EnumImageColourMode {
    /** Output image in colour mode. */
    ICM_COLOUR = 0,
    /** Output image in grayscale mode. */
    ICM_GRAYSCALE = 1,
    /** Output image in binary mode. */
    ICM_BINARY = 2
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageColourMode {
    /** Output colour image.*/
    public static final int ICM_COLOUR = 0;
    /** Output grayscale image.*/
    public static final int ICM_GRAYSCALE = 1;
    /** Output binary image.*/
    public static final int ICM_BINARY = 2;
    public EnumImageColourMode() {
    }
}
```
>
```swift
typedef NS_ENUM(NSInteger , DSImageColourMode)
{
    /** Output colour image.*/
    DSImageColourModeColour = 0x01,
    /** Output grayscale image.*/
    DSImageColourModeGrayscale = 0x02,
    /** Output binary image.*/
    DSImageColourModeBinary = 0x04

}NS_SWIFT_NAME(ImageColourMode);
```
>
```cpp
typedef enum ImageColourMode
{
    /** Output image in colour mode. */
    ICM_COLOUR = 0,    
    /** Output image in grayscale mode. */
    ICM_GRAYSCALE = 1,     
    /** Output image in binary mode. */
    ICM_BINARY = 2
} ImageColourMode;
```
