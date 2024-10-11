---
layout: default-layout
title: LogMode - Dynamsoft Core Enumerations
description: The enumeration LogMode of Dynamsoft Core describes the logging mode of the library.
keywords: logging mode
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: LogMode
codeAutoHeight: true
---

# Enumeration LogMode

`LogMode` describes the logging modes.

<div class="sample-code-prefix template2"></div>
   >- Android
   >- Objective-C
   >- Swift
   >
>
```java
public @interface EnumLogMode
{
    public static final int LGM_CONSOLE = 1;
    public static final int LGM_FILE = 2;
}
```
>
```objc
typedef NS_ENUM(NSInteger, DSLogMode)
{
    /**
     * Output the log information in the console.
     */
    DSLogModeConsole = 1,
    /**
     * Output the log information to a log file.
     */
    DSLogModeFile = 2,
};
```
>
```swift
public enum LogMode : Int
{
   /**
    * Output the log information in the console.
    */
   console = 0x01
   /**
    * Output the log information to a log file.
    */
   file = 0x02
};
```
