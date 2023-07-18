---
layout: default-layout
Title: CornerType - Dynamsoft Core Enumerations
Description: The enumeration CornerType of Dynamsoft Core describes how the corner is formed by its sides.
Keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CornerType
---

# Enumeration CornerType

`CornerType` describes how the corner is formed by its sides.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
export enum EnumCornerType
{
   /** The corner is formed by two intersecting line segments. */
   CT_NORMAL_INTERSECTED = 0,
   /** The corner is formed by two T intersecting line segments. */
   CT_T_INTERSECTED = 1,
   /** The corner is formed by two cross intersecting line segments. */
   CT_CROSS_INTERSECTED = 2,
   /** The two line segments are not intersected but they definitely consist a corner. */
   CT_NOT_INTERSECTED = 3
}
```
>
```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumCornerType
{
   /** The corner is formed by two intersecting line segments. */
   public static final int CT_NORMAL_INTERSECTED = 0;
   /** The corner is formed by two T intersecting line segments. */
   public static final int CT_T_INTERSECTED = 1;
   /** The corner is formed by two cross intersecting line segments. */
   public static final int CT_CROSS_INTERSECTED = 2;
   /** The two line segments are not intersected but they definitely consist a corner. */
   public static final int CT_NOT_INTERSECTED = 3;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSCornerType)
{
   /** The corner is formed by two intersecting line segments. */
   DSCornerTypeNormalIntersected,
   /** The corner is formed by two T intersecting line segments. */
   DSCornerTypeTIntersected,
   /** The corner is formed by two cross intersecting line segments. */
   DSCornerTypeCrossIntersected,
   /** The two line segments are not intersected but they definitely consist a corner. */
   DSCornerTypeNotIntersected
};
```
>
```swift
public enum CornerType : Int
{
   /** The corner is formed by two intersecting line segments. */
   intersected
   /** The corner is formed by two T intersecting line segments. */
   tIntersected
   /** The corner is formed by two cross intersecting line segments. */
   crossIntersected
   /** The two line segments are not intersected but they definitely consist a corner. */
   notIntersected
};
```
>
```cpp
typedef enum CornerType
{
   /* The sides of the corner is normally intersected. */
   CT_NORMAL_INTERSECTED = 0,
   /* The sides of the corner is T-intersected. */
   CT_T_INTERSECTED = 1,
   /* The sides of the corner is cross-intersected. */
   CT_CROSS_INTERSECTED = 2,
   /* The sides are not intersected but they definitely make up a corner. */
   CT_NOT_INTERSECTED = 3,
} CornerType;
```
