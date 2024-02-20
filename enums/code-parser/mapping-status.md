---
layout: default-layout
title: MappingStatus - Dynamsoft Code Parser Enumerations
description: The enumeration MappingStatus of Dynamsoft Code Parser represents the outcome of a mapping operation on a field.
keywords: Mapping status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: MappingStatus
---

# Enumeration MappingStatus

`MappingStatus` represents the outcome of a mapping operation on a field.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumMappingStatus {
    /** 
     * Indicates that no mapping operation has been initiated.
     */
    MS_NONE = 0,
    /** 
     * Indicates that the mapping operation was successfully completed.
     */
    MS_SUCCEEDED = 1,
    /** 
     * Indicates that the mapping operation failed to complete.
     */
    MS_FAILED = 2
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumMappingStatus {
   /** The field has no mapping specified. */
   public static final int MS_NONE = 0;
   /** Find a mapping for the field value. */
   public static final int MS_SUCCEEDED = 1;
   /** Failed to find a mapping for the field value. */
   public static final int MS_FAILED = 2;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSMappingStatus)
{
   /** The field has no mapping specified. */
   DSMappingStatusNotSpecified = 0,
   /** Find a mapping for the field value. */
   DSMappingStatusSucceeded = 1,
   /** Failed to find a mapping for the field value. */
   DSMappingStatusFailed = 2
};
```
>
```swift
public enum MappingStatus : Int
{
   /** The field has no mapping specified. */
   none = 0
   /** Find a mapping for the field value. */
   succeeded = 1
   /** Failed to find a mapping for the field value. */
   failed = 2
}
```
>
```cpp
typedef enum MappingStatus
{
   /** The field has no mapping specified. */
   MS_NONE,
   /** Find a mapping for the field value. */
   MS_SUCCEEDED,
   /** Failed to find a mapping for the field value. */
   MS_FAILED
} MappingStatus;
```
