---
layout: default-layout
title: ExtendedBarcodeResultType - Dynamsoft Barcode Reader Enumerations
description: The enumeration ExtendedBarcodeResultType of Dynamsoft Barcode Reader describes the type of the extended barcode result.
keywords: Extended barcode result type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ExtendedBarcodeResultType
codeAutoHeight: true
---

# Enumeration ExtendedBarcodeResultType

`ExtendedBarcodeResultType` determines the type of text result returned from a barcode scan.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >- C#
   >- Python
   >
>
```javascript
enum EnumExtendedBarcodeResultType
{
   /**Specifies the standard text. This means the barcode value. */
   EBRT_STANDARD_RESULT = 0,
   /**Specifies all the candidate text. This means all the standard text results decoded from the barcode. */
   EBRT_CANDIDATE_RESULT = 1,
   /**Specifies the partial text. This means part of the text result decoded from the barcode. */
   EBRT_PARTIAL_RESULT = 2
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumExtendedBarcodeResultType
{
   /**Specifies the standard text. This means the barcode value. */
   public static final int EBRT_STANDARD_RESULT = 0;
   /**Specifies all the candidate text. This means all the standard text results decoded from the barcode. */
   public static final int EBRT_CANDIDATE_RESULT = 1;
   /**Specifies the partial text. This means part of the text result decoded from the barcode. */
   public static final int EBRT_PARTIAL_RESULT = 2;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSExtendedBarcodeResultType)
{
   /**Specifies the standard text. This means the barcode value. */
   DSExtendedBarcodeResultTypeStandardResult = 0,
   /**Specifies all the candidate text. This means all the standard text results decoded from the barcode. */
   DSExtendedBarcodeResultTypeCandidateResult = 1,
   /**Specifies the partial text. This means part of the text result decoded from the barcode. */
   DSExtendedBarcodeResultTypePartialResult = 2
};
```
>
```swift
public enum ExtendedBarcodeResultType : Int
{
   /**Specifies the standard text. This means the barcode value. */
   standardResult = 0
   /**Specifies all the candidate text. This means all the standard text results decoded from the barcode. */
   candidateResult = 1
   /**Specifies the partial text. This means part of the text result decoded from the barcode. */
   partialResult = 2
}
```
>
```cpp
typedef enum ExtendedBarcodeResultType
{
   /**Specifies the standard text. This means the barcode value. */
   EBRT_STANDARD_RESULT,
   /**Specifies all the candidate text. This means all the standard text results decoded from the barcode. */
   EBRT_CANDIDATE_RESULT,
   /**Specifies the partial text. This means part of the text result decoded from the barcode. */
   EBRT_PARTIAL_RESULT
}ExtendedBarcodeResultType;
```
>
```csharp
public enum EnumExtendedBarcodeResultType
{
    /**Specifies the standard text. This means the barcode value. */
    EBRT_STANDARD_RESULT,
    /**Specifies all the candidate text. This means all the standard text results decoded from the barcode. */
    EBRT_CANDIDATE_RESULT,
    /**Specifies the partial text. This means part of the text result decoded from the barcode. */
    EBRT_PARTIAL_RESULT
}
```
>
```python
class EnumExtendedBarcodeResultType(IntEnum):
    #Specifies the standard text. This means the barcode value. 
    EBRT_STANDARD_RESULT
    #Specifies all the candidate text. This means all the standard text results decoded from the barcode. 
    EBRT_CANDIDATE_RESULT
    #Specifies the partial text. This means part of the text result decoded from the barcode. 
    EBRT_PARTIAL_RESULT
```
