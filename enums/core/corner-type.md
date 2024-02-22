---
layout: default-layout
title: CornerType - Dynamsoft Core Enumerations
description: The enumeration CornerType of Dynamsoft Core describes how the corner is formed by its sides.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CornerType
codeAutoHeight: true
---

# Enumeration CornerType

`CornerType` categorizes the nature of a corner based on the intersection of its adjoining sides.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >- Android
   >- Objective-C
   >- Swift
   >- C++
   >
>
```javascript
enum EnumCornerType {
    /**
     * Represents a corner formed by the standard intersection of two line segments at a point, creating a typical corner shape.
     * This is the most common corner type, where the angle between the line segments can vary from acute to obtuse.
     */
    CT_NORMAL_INTERSECTED = 0,
    /**
     * Describes a corner where two line segments intersect in a T-shape.
     * This occurs when one line segment terminates at the midpoint of another, creating three distinct angles.
     */
    CT_T_INTERSECTED = 1,
    /**
     * Characterizes a corner formed by two line segments intersecting each other in a cross shape.
     * This configuration results in four angles and is commonly encountered in grid or lattice patterns.
     */
    CT_CROSS_INTERSECTED = 2,
    /**
     * Defines a scenario where two line segments do not physically intersect but conceptually form a corner.
     * This can occur in virtual shapes or when the corner is implied by the continuation of lines beyond their endpoints.
     */
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
